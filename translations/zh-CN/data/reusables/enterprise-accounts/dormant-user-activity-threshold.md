{% ifversion not ghec%}默认情况下，如果{% else %}{% endif %} 用户帐户在 90 天内未处于活动状态，则该用户帐户被视为处于休眠状态。 {% ifversion not ghec %}您可以配置用户必须处于非活动状态才能被视为休眠{% ifversion ghes%} 的时间长度，并选择挂起休眠用户以释放用户许可证{% endif %}。{% endif %}