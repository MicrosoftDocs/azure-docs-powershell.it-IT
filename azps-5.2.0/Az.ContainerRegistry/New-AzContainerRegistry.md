---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350983"
---
# <span data-ttu-id="80054-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80054-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="80054-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80054-102">SYNOPSIS</span></span>
<span data-ttu-id="80054-103">Crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="80054-103">Creates a container registry.</span></span>

## <span data-ttu-id="80054-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80054-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80054-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80054-105">DESCRIPTION</span></span>
<span data-ttu-id="80054-106">Il cmdlet New-AzContainerRegistry crea un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="80054-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="80054-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80054-107">EXAMPLES</span></span>

### <span data-ttu-id="80054-108">Esempio 1: creare un registro di sistema contenitore con un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="80054-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="80054-109">Questo comando crea un registro di sistema contenitore con un nuovo account di archiviazione nel gruppo di risorse \` MyResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="80054-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="80054-110">Esempio 2: creare un registro dei contenitori con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="80054-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="80054-111">Questo comando crea un registro di sistema contenitore con l'utente di amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="80054-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="80054-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80054-112">PARAMETERS</span></span>

### <span data-ttu-id="80054-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80054-113">-DefaultProfile</span></span>
<span data-ttu-id="80054-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="80054-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80054-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="80054-115">-EnableAdminUser</span></span>
<span data-ttu-id="80054-116">Abilitare l'utente amministratore per il registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="80054-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="80054-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="80054-117">-Location</span></span>
<span data-ttu-id="80054-118">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="80054-118">Container Registry Location.</span></span>
<span data-ttu-id="80054-119">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80054-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="80054-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="80054-120">-Name</span></span>
<span data-ttu-id="80054-121">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="80054-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="80054-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80054-122">-ResourceGroupName</span></span>
<span data-ttu-id="80054-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="80054-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="80054-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="80054-124">-Sku</span></span>
<span data-ttu-id="80054-125">SKU del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="80054-125">Container Registry SKU.</span></span>
<span data-ttu-id="80054-126">Valori consentiti: base.</span><span class="sxs-lookup"><span data-stu-id="80054-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80054-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="80054-127">-Tag</span></span>
<span data-ttu-id="80054-128">Tag del registro di sistema contenitore. coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="80054-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="80054-129">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="80054-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="80054-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80054-130">-Confirm</span></span>
<span data-ttu-id="80054-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80054-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80054-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80054-132">-WhatIf</span></span>
<span data-ttu-id="80054-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80054-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80054-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80054-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80054-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80054-135">CommonParameters</span></span>
<span data-ttu-id="80054-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80054-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80054-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80054-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80054-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80054-138">INPUTS</span></span>

### <span data-ttu-id="80054-139">System. String</span><span class="sxs-lookup"><span data-stu-id="80054-139">System.String</span></span>

## <span data-ttu-id="80054-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80054-140">OUTPUTS</span></span>

### <span data-ttu-id="80054-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80054-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="80054-142">Note</span><span class="sxs-lookup"><span data-stu-id="80054-142">NOTES</span></span>

## <span data-ttu-id="80054-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80054-143">RELATED LINKS</span></span>

[<span data-ttu-id="80054-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80054-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="80054-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80054-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="80054-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="80054-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

