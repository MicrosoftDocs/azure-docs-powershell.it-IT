---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: b70e4b4c184cfb6ebc5473cb0f49dec712bc62fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685438"
---
# <span data-ttu-id="c2a71-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2a71-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="c2a71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2a71-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a71-103">Crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c2a71-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2a71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2a71-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2a71-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2a71-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a71-106">Il cmdlet New-AzureRmContainerRegistry crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c2a71-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="c2a71-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2a71-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a71-108">Esempio 1: creare un registro di sistema contenitore con un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c2a71-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c2a71-109">Questo comando crea un registro di sistema contenitore con un nuovo account di archiviazione nel gruppo di risorse \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="c2a71-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="c2a71-110">Esempio 2: creare un registro dei contenitori con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="c2a71-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c2a71-111">Questo comando crea un registro di sistema contenitore con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="c2a71-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="c2a71-112">Esempio 3: creare un registro dei contenitori con un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c2a71-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c2a71-113">Questo comando crea un registro di sistema con un account di archiviazione esistente \` mystorageaccount \` nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c2a71-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="c2a71-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2a71-114">PARAMETERS</span></span>

### <span data-ttu-id="c2a71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a71-115">-DefaultProfile</span></span>
<span data-ttu-id="c2a71-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c2a71-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2a71-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="c2a71-117">-EnableAdminUser</span></span>
<span data-ttu-id="c2a71-118">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="c2a71-118">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a71-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c2a71-119">-Location</span></span>
<span data-ttu-id="c2a71-120">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c2a71-120">Container Registry Location.</span></span>
<span data-ttu-id="c2a71-121">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2a71-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="c2a71-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2a71-122">-Name</span></span>
<span data-ttu-id="c2a71-123">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c2a71-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="c2a71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a71-124">-ResourceGroupName</span></span>
<span data-ttu-id="c2a71-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2a71-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2a71-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="c2a71-126">-Sku</span></span>
<span data-ttu-id="c2a71-127">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c2a71-127">Container Registry SKU.</span></span>
<span data-ttu-id="c2a71-128">Valori consentiti: base.</span><span class="sxs-lookup"><span data-stu-id="c2a71-128">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a71-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2a71-129">-StorageAccountName</span></span>
<span data-ttu-id="c2a71-130">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c2a71-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="c2a71-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2a71-131">-Tag</span></span>
<span data-ttu-id="c2a71-132">Tag del registro di sistema contenitore. coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c2a71-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="c2a71-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c2a71-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c2a71-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2a71-134">-Confirm</span></span>
<span data-ttu-id="c2a71-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2a71-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a71-136">-WhatIf</span></span>
<span data-ttu-id="c2a71-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2a71-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a71-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2a71-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a71-139">CommonParameters</span></span>
<span data-ttu-id="c2a71-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2a71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a71-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2a71-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a71-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2a71-142">INPUTS</span></span>

### <span data-ttu-id="c2a71-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c2a71-143">System.String</span></span>

## <span data-ttu-id="c2a71-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2a71-144">OUTPUTS</span></span>

### <span data-ttu-id="c2a71-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2a71-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c2a71-146">Note</span><span class="sxs-lookup"><span data-stu-id="c2a71-146">NOTES</span></span>

## <span data-ttu-id="c2a71-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2a71-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2a71-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2a71-148">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="c2a71-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2a71-149">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="c2a71-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c2a71-150">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

