---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511263"
---
# <span data-ttu-id="8b5af-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b5af-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="8b5af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b5af-102">SYNOPSIS</span></span>
<span data-ttu-id="8b5af-103">Crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b5af-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b5af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b5af-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b5af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b5af-105">DESCRIPTION</span></span>
<span data-ttu-id="8b5af-106">Il cmdlet **New-AzureRmContainerRegistry** crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b5af-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="8b5af-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b5af-107">EXAMPLES</span></span>

### <span data-ttu-id="8b5af-108">Esempio 1: creare un registro di sistema contenitore con un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8b5af-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="8b5af-109">Questo comando crea un registro di sistema contenitore con un nuovo account di archiviazione nel gruppo risorse `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="8b5af-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="8b5af-110">Esempio 2: creare un registro dei contenitori con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="8b5af-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="8b5af-111">Questo comando crea un registro di sistema contenitore con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="8b5af-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="8b5af-112">Esempio 3: creare un registro dei contenitori con un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="8b5af-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

<span data-ttu-id="8b5af-113">Questo comando crea un registro di sistema contenitore con un account `mystorageaccount` di archiviazione esistente nella stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8b5af-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="8b5af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b5af-114">PARAMETERS</span></span>

### <span data-ttu-id="8b5af-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="8b5af-115">-EnableAdminUser</span></span>
<span data-ttu-id="8b5af-116">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="8b5af-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8b5af-117">-Location</span></span>
<span data-ttu-id="8b5af-118">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b5af-118">Container Registry Location.</span></span>
<span data-ttu-id="8b5af-119">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b5af-119">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b5af-120">-Name</span></span>
<span data-ttu-id="8b5af-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b5af-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b5af-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b5af-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b5af-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="8b5af-124">-Sku</span></span>
<span data-ttu-id="8b5af-125">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b5af-125">Container Registry SKU.</span></span>
<span data-ttu-id="8b5af-126">Valori consentiti: base.</span><span class="sxs-lookup"><span data-stu-id="8b5af-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b5af-127">-StorageAccountName</span></span>
<span data-ttu-id="8b5af-128">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="8b5af-128">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b5af-129">-Tag</span></span>
<span data-ttu-id="8b5af-130">Tag del registro di sistema contenitore. coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8b5af-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8b5af-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="8b5af-131">For example:</span></span>

<span data-ttu-id="8b5af-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8b5af-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b5af-133">-Confirm</span></span>
<span data-ttu-id="8b5af-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b5af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b5af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b5af-135">-WhatIf</span></span>
<span data-ttu-id="8b5af-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b5af-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b5af-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b5af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b5af-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b5af-138">-DefaultProfile</span></span>
<span data-ttu-id="8b5af-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b5af-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b5af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b5af-140">CommonParameters</span></span>
<span data-ttu-id="8b5af-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b5af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b5af-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b5af-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b5af-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b5af-143">INPUTS</span></span>

## <span data-ttu-id="8b5af-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b5af-144">OUTPUTS</span></span>

### <span data-ttu-id="8b5af-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b5af-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="8b5af-146">Note</span><span class="sxs-lookup"><span data-stu-id="8b5af-146">NOTES</span></span>

## <span data-ttu-id="8b5af-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b5af-147">RELATED LINKS</span></span>

[<span data-ttu-id="8b5af-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b5af-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="8b5af-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b5af-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="8b5af-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8b5af-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
