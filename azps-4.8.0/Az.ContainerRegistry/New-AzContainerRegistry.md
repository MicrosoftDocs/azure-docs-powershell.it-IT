---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 1c546894cf9b11dcb65fb12b9b0575e2fd3191fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190356"
---
# <span data-ttu-id="670c7-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="670c7-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="670c7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="670c7-102">SYNOPSIS</span></span>
<span data-ttu-id="670c7-103">Crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="670c7-103">Creates a container registry.</span></span>

## <span data-ttu-id="670c7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="670c7-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670c7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="670c7-105">DESCRIPTION</span></span>
<span data-ttu-id="670c7-106">Il cmdlet New-AzContainerRegistry crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="670c7-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="670c7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="670c7-107">EXAMPLES</span></span>

### <span data-ttu-id="670c7-108">Esempio 1: creare un registro di sistema contenitore con un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="670c7-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="670c7-109">Questo comando crea un registro di sistema contenitore con un nuovo account di archiviazione nel gruppo di risorse \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="670c7-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="670c7-110">Esempio 2: creare un registro dei contenitori con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="670c7-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="670c7-111">Questo comando crea un registro di sistema contenitore con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="670c7-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="670c7-112">Esempio 3: creare un registro dei contenitori con un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="670c7-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="670c7-113">Questo comando crea un registro di sistema con un account di archiviazione esistente \` mystorageaccount \` nello stesso abbonamento.</span><span class="sxs-lookup"><span data-stu-id="670c7-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="670c7-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="670c7-114">PARAMETERS</span></span>

### <span data-ttu-id="670c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670c7-115">-DefaultProfile</span></span>
<span data-ttu-id="670c7-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="670c7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="670c7-117">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="670c7-117">-EnableAdminUser</span></span>
<span data-ttu-id="670c7-118">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="670c7-118">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="670c7-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="670c7-119">-Location</span></span>
<span data-ttu-id="670c7-120">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="670c7-120">Container Registry Location.</span></span>
<span data-ttu-id="670c7-121">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="670c7-121">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="670c7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="670c7-122">-Name</span></span>
<span data-ttu-id="670c7-123">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="670c7-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="670c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="670c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="670c7-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="670c7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="670c7-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="670c7-126">-Sku</span></span>
<span data-ttu-id="670c7-127">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="670c7-127">Container Registry SKU.</span></span>
<span data-ttu-id="670c7-128">Valori consentiti: base.</span><span class="sxs-lookup"><span data-stu-id="670c7-128">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="670c7-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="670c7-129">-StorageAccountName</span></span>
<span data-ttu-id="670c7-130">Nome di un account di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="670c7-130">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="670c7-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="670c7-131">-Tag</span></span>
<span data-ttu-id="670c7-132">Tag del registro di sistema contenitore. coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="670c7-132">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="670c7-133">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="670c7-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="670c7-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="670c7-134">-Confirm</span></span>
<span data-ttu-id="670c7-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="670c7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="670c7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670c7-136">-WhatIf</span></span>
<span data-ttu-id="670c7-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="670c7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="670c7-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="670c7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="670c7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670c7-139">CommonParameters</span></span>
<span data-ttu-id="670c7-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="670c7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670c7-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="670c7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670c7-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="670c7-142">INPUTS</span></span>

### <span data-ttu-id="670c7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="670c7-143">System.String</span></span>

## <span data-ttu-id="670c7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="670c7-144">OUTPUTS</span></span>

### <span data-ttu-id="670c7-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="670c7-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="670c7-146">Note</span><span class="sxs-lookup"><span data-stu-id="670c7-146">NOTES</span></span>

## <span data-ttu-id="670c7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="670c7-147">RELATED LINKS</span></span>

[<span data-ttu-id="670c7-148">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="670c7-148">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="670c7-149">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="670c7-149">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="670c7-150">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="670c7-150">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)
