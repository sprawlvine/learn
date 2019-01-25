
# option
+ **Callbacks for Validation**<br>
Example:
	```
    def validate_rolls(ctx, param, value):
        try:
            rolls, dice = map(int, value.split('d', 2))
            return (dice, rolls)
        except ValueError:
            raise click.BadParameter('rolls need to be in format NdM')
    
    @click.command()
    @click.option('--rolls', callback=validate_rolls, default='1d6')
    def roll(rolls):
        click.echo('Rolling a %d-sided dice %d time(s)' % rolls)
    
    if __name__ == '__main__':
        roll()
	```
And what it looks like:
	```	
    $ roll --rolls=42
    Usage: roll [OPTIONS]
    
    Error: Invalid value for "--rolls": rolls need to be in format NdM
    
    $ roll --rolls=2d12
    Rolling a 12-sided dice 2 time(s)
	```
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjAwMTE1OTY0NCwxNTQzNTQ1MDYzLDczMD
k5ODExNl19
-->