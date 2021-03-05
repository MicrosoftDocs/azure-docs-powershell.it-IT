---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: c96b1b9a7eb715f2ab7f02c7e3f86191ac756296
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992402"
---
# <span data-ttu-id="b7cd3-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b7cd3-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="b7cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="b7cd3-103">Abilita l'autenticazione di Azure AD solo per una SQL gestita specifica.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="b7cd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7cd3-104">SYNTAX</span></span>

### <span data-ttu-id="b7cd3-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b7cd3-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7cd3-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7cd3-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7cd3-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7cd3-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7cd3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b7cd3-108">DESCRIPTION</span></span>
<span data-ttu-id="b7cd3-109">Il cmdlet **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** abilita il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un'istanza gestita di AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="b7cd3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7cd3-110">EXAMPLES</span></span>

### <span data-ttu-id="b7cd3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7cd3-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="b7cd3-112">Questo comando abilita il requisito di autenticazione di Azure Active Directory (Azure AD) solo per un'istanza gestita di AzureSQL denominata ManagedInstance01 associata a un gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="b7cd3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7cd3-113">PARAMETERS</span></span>

### <span data-ttu-id="b7cd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7cd3-114">-DefaultProfile</span></span>
<span data-ttu-id="b7cd3-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7cd3-116">-InputObject</span></span>
<span data-ttu-id="b7cd3-117">L'oggetto istanza gestita da usare.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b7cd3-118">-InstanceName</span></span>
<span data-ttu-id="b7cd3-119">Nome dell'istanza gestita di Azure SQL cui si trova solo l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7cd3-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7cd3-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7cd3-122">-ResourceId</span></span>
<span data-ttu-id="b7cd3-123">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="b7cd3-123">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7cd3-124">-Confirm</span></span>
<span data-ttu-id="b7cd3-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7cd3-126">-WhatIf</span></span>
<span data-ttu-id="b7cd3-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7cd3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7cd3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7cd3-129">CommonParameters</span></span>
<span data-ttu-id="b7cd3-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7cd3-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7cd3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7cd3-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b7cd3-132">INPUTS</span></span>

### <span data-ttu-id="b7cd3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b7cd3-133">System.String</span></span>

## <span data-ttu-id="b7cd3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7cd3-134">OUTPUTS</span></span>

### <span data-ttu-id="b7cd3-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="b7cd3-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="b7cd3-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="b7cd3-136">NOTES</span></span>

## <span data-ttu-id="b7cd3-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7cd3-137">RELATED LINKS</span></span>

[<span data-ttu-id="b7cd3-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b7cd3-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="b7cd3-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="b7cd3-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="b7cd3-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7cd3-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="b7cd3-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="b7cd3-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)