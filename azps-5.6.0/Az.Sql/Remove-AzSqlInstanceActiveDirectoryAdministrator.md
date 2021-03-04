---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 16a2250941ba0e28d40648ed2cd69fee7ffefc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955149"
---
# <span data-ttu-id="6dc18-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6dc18-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="6dc18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dc18-102">SYNOPSIS</span></span>
<span data-ttu-id="6dc18-103">Rimuove un amministratore di Azure AD per SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="6dc18-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="6dc18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dc18-104">SYNTAX</span></span>

### <span data-ttu-id="6dc18-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="6dc18-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dc18-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dc18-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6dc18-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dc18-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dc18-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6dc18-108">DESCRIPTION</span></span>
<span data-ttu-id="6dc18-109">Il cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** rimuove un amministratore di Azure Active Directory (Azure AD) per l'istanza gestita di AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6dc18-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="6dc18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dc18-110">EXAMPLES</span></span>

### <span data-ttu-id="6dc18-111">Esempio 1: Rimuovere un amministratore</span><span class="sxs-lookup"><span data-stu-id="6dc18-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6dc18-112">Questo comando rimuove l'amministratore di Azure AD per l'istanza gestita denominata ManagedInstanceName01 associata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6dc18-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="6dc18-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6dc18-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6dc18-114">Questo comando rimuove l'amministratore di Azure AD dall'oggetto istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="6dc18-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="6dc18-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6dc18-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="6dc18-116">Questo comando rimuove l'amministratore di Azure AD usando l'identificatore di risorsa dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="6dc18-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="6dc18-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dc18-117">PARAMETERS</span></span>

### <span data-ttu-id="6dc18-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dc18-118">-DefaultProfile</span></span>
<span data-ttu-id="6dc18-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dc18-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dc18-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6dc18-120">-Force</span></span>
<span data-ttu-id="6dc18-121">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="6dc18-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dc18-122">-InputObject</span></span>
<span data-ttu-id="6dc18-123">L'oggetto istanza gestita da usare.</span><span class="sxs-lookup"><span data-stu-id="6dc18-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="6dc18-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6dc18-124">-InstanceName</span></span>
<span data-ttu-id="6dc18-125">SQL di istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="6dc18-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="6dc18-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dc18-126">-PassThru</span></span>
<span data-ttu-id="6dc18-127">Definisce se restituire o meno l'amministratore di Active Directory rimosso</span><span class="sxs-lookup"><span data-stu-id="6dc18-127">Defines whether to return the removed AD administrator</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dc18-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dc18-128">-ResourceGroupName</span></span>
<span data-ttu-id="6dc18-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6dc18-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="6dc18-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dc18-130">-ResourceId</span></span>
<span data-ttu-id="6dc18-131">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="6dc18-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="6dc18-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dc18-132">-Confirm</span></span>
<span data-ttu-id="6dc18-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dc18-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dc18-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dc18-134">-WhatIf</span></span>
<span data-ttu-id="6dc18-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dc18-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dc18-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dc18-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dc18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dc18-137">CommonParameters</span></span>
<span data-ttu-id="6dc18-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dc18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dc18-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6dc18-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dc18-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="6dc18-140">INPUTS</span></span>

### <span data-ttu-id="6dc18-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6dc18-141">System.String</span></span>

## <span data-ttu-id="6dc18-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dc18-142">OUTPUTS</span></span>

### <span data-ttu-id="6dc18-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="6dc18-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="6dc18-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="6dc18-144">NOTES</span></span>

## <span data-ttu-id="6dc18-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dc18-145">RELATED LINKS</span></span>

[<span data-ttu-id="6dc18-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6dc18-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="6dc18-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6dc18-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
