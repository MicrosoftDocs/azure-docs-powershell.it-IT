---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509940"
---
# <span data-ttu-id="f8cb6-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8cb6-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="f8cb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cb6-103">Crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8cb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8cb6-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8cb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="f8cb6-106">Il cmdlet New-AzureRmContainerRegistry crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="f8cb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8cb6-107">EXAMPLES</span></span>

### <span data-ttu-id="f8cb6-108">Esempio 1: creare un registro di sistema contenitore con un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f8cb6-109">Questo comando crea un registro di sistema contenitore con un nuovo account di archiviazione nel gruppo di risorse \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="f8cb6-110">Esempio 2: creare un registro dei contenitori con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f8cb6-111">Questo comando crea un registro di sistema contenitore con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="f8cb6-112">Esempio 3: creare un registro dei contenitori con un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f8cb6-113">Questo comando crea un registro di sistema con un account di archiviazione esistente \` mystorageaccount \` nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="f8cb6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8cb6-114">PARAMETERS</span></span>

### <span data-ttu-id="f8cb6-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="f8cb6-115">-EnableAdminUser</span></span>
<span data-ttu-id="f8cb6-116">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8cb6-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f8cb6-117">-Location</span></span>
<span data-ttu-id="f8cb6-118">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-118">Container Registry Location.</span></span>
<span data-ttu-id="f8cb6-119">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="f8cb6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f8cb6-120">-Name</span></span>
<span data-ttu-id="f8cb6-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cb6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cb6-122">-ResourceGroupName</span></span>
<span data-ttu-id="f8cb6-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8cb6-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="f8cb6-124">-Sku</span></span>
<span data-ttu-id="f8cb6-125">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-125">Container Registry SKU.</span></span>
<span data-ttu-id="f8cb6-126">Valori consentiti: base.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8cb6-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8cb6-127">-StorageAccountName</span></span>
<span data-ttu-id="f8cb6-128">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="f8cb6-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8cb6-129">-Tag</span></span>
<span data-ttu-id="f8cb6-130">Tag del registro di sistema contenitore. coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="f8cb6-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="f8cb6-131">For example:</span></span>

<span data-ttu-id="f8cb6-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f8cb6-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f8cb6-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8cb6-133">-Confirm</span></span>
<span data-ttu-id="f8cb6-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8cb6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8cb6-135">-WhatIf</span></span>
<span data-ttu-id="f8cb6-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8cb6-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8cb6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cb6-138">-DefaultProfile</span></span>
<span data-ttu-id="f8cb6-139">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f8cb6-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8cb6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cb6-140">CommonParameters</span></span>
<span data-ttu-id="f8cb6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cb6-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8cb6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cb6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8cb6-143">INPUTS</span></span>

### <span data-ttu-id="f8cb6-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8cb6-144">None</span></span>
<span data-ttu-id="f8cb6-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f8cb6-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8cb6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8cb6-146">OUTPUTS</span></span>

### <span data-ttu-id="f8cb6-147">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8cb6-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f8cb6-148">Note</span><span class="sxs-lookup"><span data-stu-id="f8cb6-148">NOTES</span></span>

## <span data-ttu-id="f8cb6-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8cb6-149">RELATED LINKS</span></span>

[<span data-ttu-id="f8cb6-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8cb6-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="f8cb6-151">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8cb6-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="f8cb6-152">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f8cb6-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

