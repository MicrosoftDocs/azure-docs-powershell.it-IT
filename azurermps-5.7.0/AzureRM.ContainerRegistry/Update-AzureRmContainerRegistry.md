---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516844"
---
# <span data-ttu-id="24ce3-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24ce3-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="24ce3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="24ce3-103">Aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="24ce3-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24ce3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24ce3-104">SYNTAX</span></span>

### <span data-ttu-id="24ce3-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24ce3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24ce3-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ce3-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ce3-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ce3-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24ce3-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ce3-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24ce3-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ce3-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24ce3-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24ce3-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24ce3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24ce3-111">DESCRIPTION</span></span>
<span data-ttu-id="24ce3-112">Il cmdlet Update-AzureRmContainerRegistry aggiorna un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="24ce3-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="24ce3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24ce3-113">EXAMPLES</span></span>

### <span data-ttu-id="24ce3-114">Esempio 1: abilitare l'utente dell'amministratore per un registro contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="24ce3-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="24ce3-115">Questo comando consente all'utente di amministratore per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="24ce3-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="24ce3-116">Esempio 2: impostare l'account di archiviazione usato da un registro dei contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="24ce3-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="24ce3-117">Questo comando imposta il registro di sistema del contenitore specificato per l'uso di un account di archiviazione esistente \` mystorageaccount \` nella stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="24ce3-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="24ce3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24ce3-118">PARAMETERS</span></span>

### <span data-ttu-id="24ce3-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="24ce3-119">-DisableAdminUser</span></span>
<span data-ttu-id="24ce3-120">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="24ce3-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="24ce3-121">-EnableAdminUser</span></span>
<span data-ttu-id="24ce3-122">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="24ce3-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="24ce3-123">-Name</span></span>
<span data-ttu-id="24ce3-124">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="24ce3-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24ce3-125">-ResourceGroupName</span></span>
<span data-ttu-id="24ce3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24ce3-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24ce3-127">-StorageAccountName</span></span>
<span data-ttu-id="24ce3-128">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="24ce3-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="24ce3-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="24ce3-129">-Tag</span></span>
<span data-ttu-id="24ce3-130">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="24ce3-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="24ce3-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="24ce3-131">For example:</span></span>

<span data-ttu-id="24ce3-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="24ce3-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24ce3-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="24ce3-133">-Confirm</span></span>
<span data-ttu-id="24ce3-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24ce3-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24ce3-135">-WhatIf</span></span>
<span data-ttu-id="24ce3-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24ce3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24ce3-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="24ce3-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24ce3-138">-DefaultProfile</span></span>
<span data-ttu-id="24ce3-139">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="24ce3-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24ce3-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24ce3-140">-ResourceId</span></span>
<span data-ttu-id="24ce3-141">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="24ce3-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="24ce3-142">-Sku</span></span>
<span data-ttu-id="24ce3-143">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="24ce3-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24ce3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24ce3-144">CommonParameters</span></span>
<span data-ttu-id="24ce3-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24ce3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24ce3-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24ce3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24ce3-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24ce3-147">INPUTS</span></span>

### <span data-ttu-id="24ce3-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="24ce3-148">None</span></span>
<span data-ttu-id="24ce3-149">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="24ce3-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24ce3-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24ce3-150">OUTPUTS</span></span>

### <span data-ttu-id="24ce3-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24ce3-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="24ce3-152">Note</span><span class="sxs-lookup"><span data-stu-id="24ce3-152">NOTES</span></span>

## <span data-ttu-id="24ce3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24ce3-153">RELATED LINKS</span></span>

[<span data-ttu-id="24ce3-154">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24ce3-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="24ce3-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24ce3-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="24ce3-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="24ce3-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

