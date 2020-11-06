---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlInstance.md
ms.openlocfilehash: 1e992e33591f5c993bfdda1bf9934245b2f5f2c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520137"
---
# <span data-ttu-id="8f67c-101">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="8f67c-101">Set-AzureRmSqlInstance</span></span>

## <span data-ttu-id="8f67c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f67c-102">SYNOPSIS</span></span>
<span data-ttu-id="8f67c-103">Imposta le proprietà per un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f67c-103">Sets properties for an Azure SQL Database Managed Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f67c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f67c-104">SYNTAX</span></span>

### <span data-ttu-id="8f67c-105">SetInstanceFromInputParameters (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8f67c-105">SetInstanceFromInputParameters (Default)</span></span>
```
Set-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f67c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="8f67c-106">SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Set-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-AdministratorPassword <SecureString>]
 [-Edition <String>] [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>]
 [-AssignIdentity] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f67c-107">SetInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="8f67c-107">SetInstanceFromAzureResourceId</span></span>
```
Set-AzureRmSqlInstance [-ResourceId] <String> [-AdministratorPassword <SecureString>] [-Edition <String>]
 [-LicenseType <String>] [-StorageSizeInGB <Int32>] [-VCore <Int32>] [-Tag <Hashtable>] [-AssignIdentity]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f67c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f67c-108">DESCRIPTION</span></span>
<span data-ttu-id="8f67c-109">Il cmdlet **set-AzureRmSqlInstance** modifica le proprietà di un'istanza gestita di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="8f67c-109">The **Set-AzureRmSqlInstance** cmdlet modifies properties of an Azure SQL Database Managed instance.</span></span>

## <span data-ttu-id="8f67c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f67c-110">EXAMPLES</span></span>

### <span data-ttu-id="8f67c-111">Esempio 1: impostare l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="8f67c-111">Example 1: Set existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>
```
PS C:\>$InstancePassword = "Newpassword1234"
PS C:\> $SecureString = ConvertTo-SecureString $InstancePassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlInstance -Name "managedinstance1" -ResourceGroupName "ResourceGroup01" -AdministratorPassword $SecureString -LicenseType LicenseIncluded -StorageSizeInGB 1024 -VCore 16
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : LicenseIncluded
VCores                   : 16
StorageSizeInGB          : 1024
```

<span data-ttu-id="8f67c-112">Questo comando imposta l'istanza esistente usando i nuovi valori per-AdministratorPassword,-LicenseType,-StorageSizeInGB e-VCore</span><span class="sxs-lookup"><span data-stu-id="8f67c-112">This command sets existing instance using new values for -AdministratorPassword, -LicenseType, -StorageSizeInGB and -VCore</span></span>

## <span data-ttu-id="8f67c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f67c-113">PARAMETERS</span></span>

### <span data-ttu-id="8f67c-114">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="8f67c-114">-AdministratorPassword</span></span>
<span data-ttu-id="8f67c-115">La nuova password di amministratore SQL per l'istanza.</span><span class="sxs-lookup"><span data-stu-id="8f67c-115">The new SQL administrator password for the instance.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8f67c-116">-AssignIdentity</span></span>
<span data-ttu-id="8f67c-117">Genera e assegna un'identità di Azure Active Directory per questa istanza per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8f67c-117">Generate and assign an Azure Active Directory Identity for this instance for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f67c-118">-DefaultProfile</span></span>
<span data-ttu-id="8f67c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f67c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="8f67c-120">-Edition</span></span>
<span data-ttu-id="8f67c-121">L'edizione da assegnare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="8f67c-121">The edition to assign to the instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8f67c-122">-Force</span></span>
<span data-ttu-id="8f67c-123">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="8f67c-123">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f67c-124">-InputObject</span></span>
<span data-ttu-id="8f67c-125">Oggetto AzureSqlManagedInstanceModel da rimuovere</span><span class="sxs-lookup"><span data-stu-id="8f67c-125">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: SetInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-126">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8f67c-126">-LicenseType</span></span>
<span data-ttu-id="8f67c-127">Determina il tipo di licenza di istanza da usare</span><span class="sxs-lookup"><span data-stu-id="8f67c-127">Determines which License Type of instance to use</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f67c-128">-Name</span></span>
<span data-ttu-id="8f67c-129">Nome istanza.</span><span class="sxs-lookup"><span data-stu-id="8f67c-129">Instance name.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f67c-130">-ResourceGroupName</span></span>
<span data-ttu-id="8f67c-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8f67c-131">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f67c-132">-ResourceId</span></span>
<span data-ttu-id="8f67c-133">ID risorsa dell'istanza da rimuovere</span><span class="sxs-lookup"><span data-stu-id="8f67c-133">The resource id of instance to remove</span></span>

```yaml
Type: String
Parameter Sets: SetInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-134">-StorageSizeInGB</span><span class="sxs-lookup"><span data-stu-id="8f67c-134">-StorageSizeInGB</span></span>
<span data-ttu-id="8f67c-135">Determina la quantità di spazio di archiviazione da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="8f67c-135">Determines how much Storage size to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f67c-136">-Tag</span></span>
<span data-ttu-id="8f67c-137">Tag da associare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="8f67c-137">The tags to associate with the instance.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-138">-VCore</span><span class="sxs-lookup"><span data-stu-id="8f67c-138">-VCore</span></span>
<span data-ttu-id="8f67c-139">Determina la quantità di VCore da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="8f67c-139">Determines how much VCore to associate with instance</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f67c-140">-Confirm</span></span>
<span data-ttu-id="8f67c-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f67c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f67c-142">-WhatIf</span></span>
<span data-ttu-id="8f67c-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f67c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f67c-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f67c-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f67c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f67c-145">CommonParameters</span></span>
<span data-ttu-id="8f67c-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f67c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f67c-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f67c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f67c-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f67c-148">INPUTS</span></span>

### <span data-ttu-id="8f67c-149">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8f67c-149">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="8f67c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="8f67c-150">System.String</span></span>

## <span data-ttu-id="8f67c-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f67c-151">OUTPUTS</span></span>

### <span data-ttu-id="8f67c-152">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="8f67c-152">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="8f67c-153">Note</span><span class="sxs-lookup"><span data-stu-id="8f67c-153">NOTES</span></span>

## <span data-ttu-id="8f67c-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f67c-154">RELATED LINKS</span></span>
