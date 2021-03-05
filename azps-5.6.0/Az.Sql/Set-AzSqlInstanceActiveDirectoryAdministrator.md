---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: a8c748e2d37dbb4759df27b56b37719bcbb2babf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015854"
---
# <span data-ttu-id="1110b-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1110b-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="1110b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1110b-102">SYNOPSIS</span></span>
<span data-ttu-id="1110b-103">Esegue il provisioning di un amministratore di Azure AD SQL'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1110b-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="1110b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1110b-104">SYNTAX</span></span>

### <span data-ttu-id="1110b-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="1110b-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1110b-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1110b-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 -InputObject <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1110b-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1110b-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1110b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1110b-108">DESCRIPTION</span></span>
<span data-ttu-id="1110b-109">Il cmdlet **Set-AzSqlInstanceActiveDirectoryAdministrator** esegue il provisioning di un amministratore di Azure Active Directory (Azure AD) per l'istanza gestita di AzureSQL nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1110b-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="1110b-110">È possibile eseguire il provisioning di un solo amministratore alla volta.</span><span class="sxs-lookup"><span data-stu-id="1110b-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="1110b-111">È possibile eseguire il provisioning dei membri seguenti di Azure AD come amministratore SQL istanza gestita:</span><span class="sxs-lookup"><span data-stu-id="1110b-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="1110b-112">Membri nativi di Azure AD</span><span class="sxs-lookup"><span data-stu-id="1110b-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="1110b-113">Membri federati di Azure AD</span><span class="sxs-lookup"><span data-stu-id="1110b-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="1110b-114">I gruppi di Azure AD creati come gruppi di sicurezza importati membri da altri AZURE ADS non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="1110b-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="1110b-115">Gli account Microsoft, ad esempio quelli nei domini Outlook.com, Hotmail.com o Live.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="1110b-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="1110b-116">Gli altri account guest, ad esempio quelli nel dominio Gmail.com o Yahoo.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="1110b-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="1110b-117">È consigliabile eseguire il provisioning di un gruppo di Azure AD dedicato come amministratore.</span><span class="sxs-lookup"><span data-stu-id="1110b-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="1110b-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1110b-118">EXAMPLES</span></span>

### <span data-ttu-id="1110b-119">Esempio 1: Eseguire il provisioning di un gruppo di amministratori per un'istanza gestita associata al gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1110b-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="1110b-120">Questo comando esegue il provisioning di un gruppo di amministratori di Azure AD denominato DBA per l'istanza gestita denominata ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="1110b-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="1110b-121">Questo server è associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="1110b-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="1110b-122">Esempio 2: Effettuare il provisioning di un utente amministratore usando un oggetto istanza gestita</span><span class="sxs-lookup"><span data-stu-id="1110b-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="1110b-123">Questo comando esegue il provisioning di un utente di Azure AD come amministratore dall'oggetto dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1110b-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="1110b-124">Esempio 3: Eseguire il provisioning di un amministratore usando l'identificatore di risorsa dell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="1110b-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/managedInstances/ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdministrator -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
Resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="1110b-125">Questo comando esegue il provisioning di un utente di Azure AD come amministratore usando l'identificatore di risorsa dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1110b-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="1110b-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1110b-126">PARAMETERS</span></span>

### <span data-ttu-id="1110b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1110b-127">-DefaultProfile</span></span>
<span data-ttu-id="1110b-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1110b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1110b-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1110b-129">-DisplayName</span></span>
<span data-ttu-id="1110b-130">Specifica il nome visualizzato dell'utente o del gruppo a cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="1110b-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="1110b-131">Questo nome visualizzato deve essere in Active Directory associato all'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="1110b-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1110b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1110b-132">-InputObject</span></span>
<span data-ttu-id="1110b-133">L'oggetto istanza gestita da usare.</span><span class="sxs-lookup"><span data-stu-id="1110b-133">The managed instance object to use.</span></span>

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

### <span data-ttu-id="1110b-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="1110b-134">-InstanceName</span></span>
<span data-ttu-id="1110b-135">SQL di istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="1110b-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="1110b-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1110b-136">-ObjectId</span></span>
<span data-ttu-id="1110b-137">Specifica l'ID oggetto dell'utente o gruppo in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="1110b-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1110b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1110b-138">-ResourceGroupName</span></span>
<span data-ttu-id="1110b-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1110b-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="1110b-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1110b-140">-ResourceId</span></span>
<span data-ttu-id="1110b-141">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="1110b-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="1110b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1110b-142">-Confirm</span></span>
<span data-ttu-id="1110b-143">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1110b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1110b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1110b-144">-WhatIf</span></span>
<span data-ttu-id="1110b-145">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1110b-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1110b-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1110b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1110b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1110b-147">CommonParameters</span></span>
<span data-ttu-id="1110b-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1110b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1110b-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1110b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1110b-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="1110b-150">INPUTS</span></span>

### <span data-ttu-id="1110b-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1110b-151">System.String</span></span>

### <span data-ttu-id="1110b-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1110b-152">System.Guid</span></span>

## <span data-ttu-id="1110b-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1110b-153">OUTPUTS</span></span>

### <span data-ttu-id="1110b-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="1110b-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="1110b-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="1110b-155">NOTES</span></span>

## <span data-ttu-id="1110b-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1110b-156">RELATED LINKS</span></span>

[<span data-ttu-id="1110b-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1110b-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="1110b-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1110b-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
