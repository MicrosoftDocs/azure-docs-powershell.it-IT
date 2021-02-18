---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181455"
---
# <span data-ttu-id="efc8d-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="efc8d-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="efc8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc8d-102">SYNOPSIS</span></span>
<span data-ttu-id="efc8d-103">Crea un registro di contenitore.</span><span class="sxs-lookup"><span data-stu-id="efc8d-103">Creates a container registry.</span></span>

## <span data-ttu-id="efc8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efc8d-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc8d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="efc8d-105">DESCRIPTION</span></span>
<span data-ttu-id="efc8d-106">Il cmdlet New-AzContainerRegistry crea un registro di contenitore.</span><span class="sxs-lookup"><span data-stu-id="efc8d-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="efc8d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efc8d-107">EXAMPLES</span></span>

### <span data-ttu-id="efc8d-108">Esempio 1: Creare un Registro di sistema del contenitore con un nuovo account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="efc8d-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="efc8d-109">Questo comando crea un registro di contenitore con un nuovo account di archiviazione nel gruppo di risorse \` \` MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="efc8d-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="efc8d-110">Esempio 2: Creare un registro di contenitore con un utente amministratore abilitato.</span><span class="sxs-lookup"><span data-stu-id="efc8d-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="efc8d-111">Questo comando crea un registro di sistema del contenitore con l'ancoraggio degli utenti da parte dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="efc8d-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="efc8d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efc8d-112">PARAMETERS</span></span>

### <span data-ttu-id="efc8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc8d-113">-DefaultProfile</span></span>
<span data-ttu-id="efc8d-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="efc8d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efc8d-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="efc8d-115">-EnableAdminUser</span></span>
<span data-ttu-id="efc8d-116">Abilitare l'utente amministratore per il Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="efc8d-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="efc8d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="efc8d-117">-Location</span></span>
<span data-ttu-id="efc8d-118">Posizione del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="efc8d-118">Container Registry Location.</span></span>
<span data-ttu-id="efc8d-119">Impostazione predefinita per il percorso del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc8d-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="efc8d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="efc8d-120">-Name</span></span>
<span data-ttu-id="efc8d-121">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="efc8d-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="efc8d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc8d-122">-ResourceGroupName</span></span>
<span data-ttu-id="efc8d-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="efc8d-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="efc8d-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="efc8d-124">-Sku</span></span>
<span data-ttu-id="efc8d-125">SKU container Registry.</span><span class="sxs-lookup"><span data-stu-id="efc8d-125">Container Registry SKU.</span></span>
<span data-ttu-id="efc8d-126">Valori consentiti: Base.</span><span class="sxs-lookup"><span data-stu-id="efc8d-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="efc8d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="efc8d-127">-Tag</span></span>
<span data-ttu-id="efc8d-128">Container Registry Tags.Key-value pairs in form of a hash table.</span><span class="sxs-lookup"><span data-stu-id="efc8d-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="efc8d-129">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="efc8d-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="efc8d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efc8d-130">-Confirm</span></span>
<span data-ttu-id="efc8d-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc8d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc8d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc8d-132">-WhatIf</span></span>
<span data-ttu-id="efc8d-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc8d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc8d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efc8d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc8d-135">CommonParameters</span></span>
<span data-ttu-id="efc8d-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc8d-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="efc8d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc8d-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="efc8d-138">INPUTS</span></span>

### <span data-ttu-id="efc8d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="efc8d-139">System.String</span></span>

## <span data-ttu-id="efc8d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efc8d-140">OUTPUTS</span></span>

### <span data-ttu-id="efc8d-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="efc8d-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="efc8d-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="efc8d-142">NOTES</span></span>

## <span data-ttu-id="efc8d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efc8d-143">RELATED LINKS</span></span>

[<span data-ttu-id="efc8d-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="efc8d-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="efc8d-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="efc8d-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="efc8d-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="efc8d-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

