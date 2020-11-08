---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 361517912166c9548ecc69358c6dd0e776cfcd3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202267"
---
# <span data-ttu-id="9c718-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9c718-101">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="9c718-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c718-102">SYNOPSIS</span></span>
<span data-ttu-id="9c718-103">Rimuove un amministratore di Azure AD per l'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="9c718-103">Removes an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="9c718-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c718-104">SYNTAX</span></span>

### <span data-ttu-id="9c718-105">UseResourceGroupAndInstanceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c718-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c718-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c718-106">UseInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru]
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c718-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c718-107">UserResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceActiveDirectoryAdministrator [-Force] [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c718-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c718-108">DESCRIPTION</span></span>
<span data-ttu-id="9c718-109">Il cmdlet **Remove-AzSqlInstanceActiveDirectoryAdministrator** rimuove un amministratore di Azure Active Directory (Azure ad) per l'istanza gestita di AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="9c718-109">The **Remove-AzSqlInstanceActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="9c718-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c718-110">EXAMPLES</span></span>

### <span data-ttu-id="9c718-111">Esempio 1: rimuovere un amministratore</span><span class="sxs-lookup"><span data-stu-id="9c718-111">Example 1: Remove an administrator</span></span>
```
PS C:\>Remove-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstanceName01" -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="9c718-112">Questo comando rimuove l'amministratore di Azure AD per l'istanza gestita denominata ManagedInstanceName01 associata al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="9c718-112">This command removes the Azure AD administrator for the managed instance named ManagedInstanceName01 associated with the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="9c718-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9c718-113">Example 2</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="9c718-114">Questo comando rimuove l'amministratore di Azure AD dall'oggetto istanza gestito.</span><span class="sxs-lookup"><span data-stu-id="9c718-114">This command removes the Azure AD administrator from the managed instance object.</span></span>

### <span data-ttu-id="9c718-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9c718-115">Example 3</span></span>
```powershell
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance1" | Remove-AzSqlInstanceActiveDirectoryAdministrator -Confirm -PassThru
Are you sure you want to remove the Azure Sql Instance Active Directory Administrator on managed instance 'ManagedInstanceName01'? 
[Y] Yes [A] Yes to All [N] No [L] No to All [S] Suspend [?] Help (default is "Y"): Y 

ResourceGroupName InstanceName          DisplayName ObjectId 
----------------- --------------------- ----------- -------- 
ResourceGroup01   ManagedInstanceName01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="9c718-116">Questo comando rimuove l'amministratore di Azure AD usando l'identificatore delle risorse dell'istanza gestito.</span><span class="sxs-lookup"><span data-stu-id="9c718-116">This command removes the Azure AD administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="9c718-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c718-117">PARAMETERS</span></span>

### <span data-ttu-id="9c718-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c718-118">-DefaultProfile</span></span>
<span data-ttu-id="9c718-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c718-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c718-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9c718-120">-Force</span></span>
<span data-ttu-id="9c718-121">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="9c718-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9c718-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c718-122">-InputObject</span></span>
<span data-ttu-id="9c718-123">Oggetto istanza gestito da usare.</span><span class="sxs-lookup"><span data-stu-id="9c718-123">The managed instance object to use.</span></span>

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

### <span data-ttu-id="9c718-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9c718-124">-InstanceName</span></span>
<span data-ttu-id="9c718-125">Nome dell'istanza gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="9c718-125">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="9c718-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c718-126">-PassThru</span></span>
<span data-ttu-id="9c718-127">Definisce se restituire l'amministratore di Active Directory rimosso</span><span class="sxs-lookup"><span data-stu-id="9c718-127">Defines whether to return the removed AD administrator</span></span>

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

### <span data-ttu-id="9c718-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c718-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c718-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9c718-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9c718-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c718-130">-ResourceId</span></span>
<span data-ttu-id="9c718-131">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="9c718-131">The resource id of instance to use</span></span>

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

### <span data-ttu-id="9c718-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c718-132">-Confirm</span></span>
<span data-ttu-id="9c718-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c718-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c718-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c718-134">-WhatIf</span></span>
<span data-ttu-id="9c718-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c718-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c718-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c718-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c718-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c718-137">CommonParameters</span></span>
<span data-ttu-id="9c718-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c718-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c718-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c718-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c718-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c718-140">INPUTS</span></span>

### <span data-ttu-id="9c718-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9c718-141">System.String</span></span>

## <span data-ttu-id="9c718-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c718-142">OUTPUTS</span></span>

### <span data-ttu-id="9c718-143">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="9c718-143">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="9c718-144">Note</span><span class="sxs-lookup"><span data-stu-id="9c718-144">NOTES</span></span>

## <span data-ttu-id="9c718-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c718-145">RELATED LINKS</span></span>

[<span data-ttu-id="9c718-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9c718-146">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="9c718-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="9c718-147">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)
