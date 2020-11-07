---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstanceactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceActiveDirectoryAdministrator.md
ms.openlocfilehash: 8a034bc85209e0325547bac2f64f277ceaee0abc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857229"
---
# <span data-ttu-id="ff78a-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ff78a-101">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="ff78a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff78a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff78a-103">Viene previsto un amministratore di Azure AD per l'istanza gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="ff78a-103">Provisions an Azure AD administrator for SQL Managed Instance.</span></span>

## <span data-ttu-id="ff78a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff78a-104">SYNTAX</span></span>

### <span data-ttu-id="ff78a-105">UseResourceGroupAndInstanceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff78a-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff78a-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff78a-106">UseInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid>
 [-InputObject <AzureSqlManagedInstanceModel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff78a-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff78a-107">UserResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceActiveDirectoryAdministrator [-DisplayName] <String> [-ObjectId] <Guid> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff78a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff78a-108">DESCRIPTION</span></span>
<span data-ttu-id="ff78a-109">Il cmdlet **set-AzSqlInstanceActiveDirectoryAdministrator** dispone di un amministratore di Azure Active Directory (Azure ad) per l'istanza gestita di AzureSQL nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="ff78a-109">The **Set-AzSqlInstanceActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for AzureSQL Managed Instance in the current subscription.</span></span>
<span data-ttu-id="ff78a-110">È possibile eseguire il provisioning di un solo amministratore alla volta.</span><span class="sxs-lookup"><span data-stu-id="ff78a-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="ff78a-111">I membri seguenti di Azure AD possono essere provisionati come amministratore di istanze gestite da SQL:</span><span class="sxs-lookup"><span data-stu-id="ff78a-111">The following members of Azure AD can be provisioned as a SQL Managed Instance administrator:</span></span>
- <span data-ttu-id="ff78a-112">Membri nativi di Azure AD</span><span class="sxs-lookup"><span data-stu-id="ff78a-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="ff78a-113">Membri federati di Azure AD</span><span class="sxs-lookup"><span data-stu-id="ff78a-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="ff78a-114">I gruppi di Azure AD creati come gruppi di sicurezza importati da altri annunci di Azure non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="ff78a-114">Azure AD groups created as security groups Imported members from other Azure ADs are not supported as administrators.</span></span>
<span data-ttu-id="ff78a-115">Gli account Microsoft, ad esempio quelli nei domini Outlook.com, Hotmail.com o Live.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="ff78a-115">Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="ff78a-116">Gli altri account Guest, ad esempio quelli presenti nei domini Gmail.com o Yahoo.com, non sono supportati come amministratori.</span><span class="sxs-lookup"><span data-stu-id="ff78a-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="ff78a-117">Ti consigliamo di eseguire il provisioning di un gruppo di annunci Azure dedicato come amministratore.</span><span class="sxs-lookup"><span data-stu-id="ff78a-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="ff78a-118">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff78a-118">EXAMPLES</span></span>

### <span data-ttu-id="ff78a-119">Esempio 1: eseguire il provisioning di un gruppo di amministratori per un'istanza gestita associata al gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ff78a-119">Example 1: Provision an administrator group for a managed instance associated with resource group</span></span>
```
PS C:\>Set-AzSqlInstanceActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
ResourceGroup01   ManagedInstance01 DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="ff78a-120">Questo comando serve un gruppo di amministratori di Azure AD denominato DBA per l'istanza gestita denominata ManagedInstance01.</span><span class="sxs-lookup"><span data-stu-id="ff78a-120">This command provisions an Azure AD administrator group named DBAs for the managed instance named ManagedInstance01.</span></span>
<span data-ttu-id="ff78a-121">Questo server è associato al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="ff78a-121">This server is associated with resource group ResourceGroup01.</span></span>

### <span data-ttu-id="ff78a-122">Esempio 2: eseguire il provisioning di un utente di amministratore usando l'oggetto istanza gestito</span><span class="sxs-lookup"><span data-stu-id="ff78a-122">Example 2: Provision an administrator user using managed instance object</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="ff78a-123">Questo comando serve un utente di Azure AD come amministratore dall'oggetto istanza gestito.</span><span class="sxs-lookup"><span data-stu-id="ff78a-123">This command provisions an Azure AD user as an administrator from the managed instance object.</span></span>

### <span data-ttu-id="ff78a-124">Esempio 3: eseguire il provisioning di un amministratore tramite l'identificatore di risorsa istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ff78a-124">Example 3: Provision an administrator using managed instance resource identifier</span></span>
```
PS C:\>Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" | Set-AzSqlInstanceActiveDirectoryAdmin -DisplayName "David Chew" -ObjectId "11E95548-B179-4FE1-9AF4-ACA49D13ABB9"
ResourceGroupName InstanceName      DisplayName ObjectId 
----------------- ----------------- ----------- -------- 
resourcegroup01   ManagedInstance01 David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

<span data-ttu-id="ff78a-125">Questo comando usa un utente di Azure AD come amministratore usando l'identificatore delle risorse di istanza gestito.</span><span class="sxs-lookup"><span data-stu-id="ff78a-125">This command provisions an Azure AD user as an administrator using managed instance resource identifier.</span></span>

## <span data-ttu-id="ff78a-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff78a-126">PARAMETERS</span></span>

### <span data-ttu-id="ff78a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff78a-127">-DefaultProfile</span></span>
<span data-ttu-id="ff78a-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff78a-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff78a-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ff78a-129">-DisplayName</span></span>
<span data-ttu-id="ff78a-130">Specifica il nome visualizzato dell'utente o del gruppo per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="ff78a-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="ff78a-131">Questo nome visualizzato deve esistere in Active Directory associato alla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="ff78a-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="ff78a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff78a-132">-InputObject</span></span>
<span data-ttu-id="ff78a-133">Oggetto istanza gestito da usare.</span><span class="sxs-lookup"><span data-stu-id="ff78a-133">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff78a-134">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ff78a-134">-InstanceName</span></span>
<span data-ttu-id="ff78a-135">Nome dell'istanza gestita da SQL.</span><span class="sxs-lookup"><span data-stu-id="ff78a-135">SQL Managed Instance name.</span></span>

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

### <span data-ttu-id="ff78a-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ff78a-136">-ObjectId</span></span>
<span data-ttu-id="ff78a-137">Specifica l'ID oggetto dell'utente o del gruppo in Azure Active Directory per cui concedere le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="ff78a-137">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="ff78a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff78a-138">-ResourceGroupName</span></span>
<span data-ttu-id="ff78a-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ff78a-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="ff78a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff78a-140">-ResourceId</span></span>
<span data-ttu-id="ff78a-141">ID risorsa dell'istanza da usare</span><span class="sxs-lookup"><span data-stu-id="ff78a-141">The resource id of instance to use</span></span>

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

### <span data-ttu-id="ff78a-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff78a-142">-Confirm</span></span>
<span data-ttu-id="ff78a-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff78a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff78a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff78a-144">-WhatIf</span></span>
<span data-ttu-id="ff78a-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff78a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff78a-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff78a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff78a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff78a-147">CommonParameters</span></span>
<span data-ttu-id="ff78a-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff78a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff78a-149">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff78a-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff78a-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff78a-150">INPUTS</span></span>

### <span data-ttu-id="ff78a-151">System. String</span><span class="sxs-lookup"><span data-stu-id="ff78a-151">System.String</span></span>

### <span data-ttu-id="ff78a-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="ff78a-152">System.Guid</span></span>

## <span data-ttu-id="ff78a-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff78a-153">OUTPUTS</span></span>

### <span data-ttu-id="ff78a-154">Microsoft. Azure. Commands. SQL. InstanceActiveDirectoryAdministrator. Model. AzureSqlInstanceActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="ff78a-154">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryAdministrator.Model.AzureSqlInstanceActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="ff78a-155">Note</span><span class="sxs-lookup"><span data-stu-id="ff78a-155">NOTES</span></span>

## <span data-ttu-id="ff78a-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff78a-156">RELATED LINKS</span></span>

[<span data-ttu-id="ff78a-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ff78a-157">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="ff78a-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="ff78a-158">Remove-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Remove-AzSqlInstanceActiveDirectoryAdministrator.md)
