---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520784"
---
# <span data-ttu-id="6a7e8-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a7e8-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="6a7e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a7e8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7e8-103">Aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a7e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a7e8-104">SYNTAX</span></span>

### <span data-ttu-id="6a7e8-105">Empty (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a7e8-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a7e8-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a7e8-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a7e8-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="6a7e8-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a7e8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a7e8-108">DESCRIPTION</span></span>
<span data-ttu-id="6a7e8-109">Il cmdlet **Update-AzureRmContainerRegistry** aggiorna il registro di sistema di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="6a7e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a7e8-110">EXAMPLES</span></span>

### <span data-ttu-id="6a7e8-111">Esempio 1: abilitare l'utente dell'amministratore per un registro contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="6a7e8-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="6a7e8-112">Questo comando consente all'utente di amministratore per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="6a7e8-113">Esempio 2: impostare l'account di archiviazione usato da un registro dei contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="6a7e8-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="6a7e8-114">Questo comando imposta il registro di sistema del contenitore specificato per l'uso di un account di archiviazione esistente `mystorageaccount` nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="6a7e8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a7e8-115">PARAMETERS</span></span>

### <span data-ttu-id="6a7e8-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="6a7e8-116">-DisableAdminUser</span></span>
<span data-ttu-id="6a7e8-117">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a7e8-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="6a7e8-118">-EnableAdminUser</span></span>
<span data-ttu-id="6a7e8-119">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a7e8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a7e8-120">-Name</span></span>
<span data-ttu-id="6a7e8-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="6a7e8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a7e8-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a7e8-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="6a7e8-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6a7e8-124">-StorageAccountName</span></span>
<span data-ttu-id="6a7e8-125">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="6a7e8-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a7e8-126">-Tag</span></span>
<span data-ttu-id="6a7e8-127">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a7e8-128">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="6a7e8-128">For example:</span></span>

<span data-ttu-id="6a7e8-129">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6a7e8-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6a7e8-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a7e8-130">-Confirm</span></span>
<span data-ttu-id="6a7e8-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a7e8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a7e8-132">-WhatIf</span></span>
<span data-ttu-id="6a7e8-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a7e8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a7e8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7e8-135">-DefaultProfile</span></span>
<span data-ttu-id="6a7e8-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a7e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7e8-137">CommonParameters</span></span>
<span data-ttu-id="6a7e8-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a7e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7e8-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7e8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7e8-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a7e8-140">INPUTS</span></span>

## <span data-ttu-id="6a7e8-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a7e8-141">OUTPUTS</span></span>

### <span data-ttu-id="6a7e8-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a7e8-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="6a7e8-143">Note</span><span class="sxs-lookup"><span data-stu-id="6a7e8-143">NOTES</span></span>

## <span data-ttu-id="6a7e8-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a7e8-144">RELATED LINKS</span></span>

[<span data-ttu-id="6a7e8-145">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a7e8-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="6a7e8-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a7e8-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="6a7e8-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6a7e8-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
