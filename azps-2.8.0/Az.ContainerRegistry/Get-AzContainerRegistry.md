---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: f833d2f46c67964356f48a06c35d41dfcf090fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675093"
---
# <span data-ttu-id="58c3e-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="58c3e-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="58c3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="58c3e-103">Ottiene un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="58c3e-103">Gets a container registry.</span></span>

## <span data-ttu-id="58c3e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58c3e-104">SYNTAX</span></span>

### <span data-ttu-id="58c3e-105">ListRegistriesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58c3e-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c3e-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c3e-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58c3e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58c3e-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58c3e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58c3e-108">DESCRIPTION</span></span>
<span data-ttu-id="58c3e-109">Il cmdlet Get-AzContainerRegistry ottiene un registro dei contenitori specificato o tutti i registri contenitore in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="58c3e-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="58c3e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58c3e-110">EXAMPLES</span></span>

### <span data-ttu-id="58c3e-111">Esempio 1: ottenere un registro di sistema contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="58c3e-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="58c3e-112">Questo comando ottiene il registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="58c3e-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="58c3e-113">Esempio 2: ottenere tutti i registri dei contenitori in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="58c3e-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="58c3e-114">Questo comando consente di ottenere tutti i registri contenitore in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58c3e-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="58c3e-115">Esempio 3: ottenere tutti i registri contenitore nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="58c3e-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="58c3e-116">Questo comando consente di ottenere tutti i registri contenitore nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="58c3e-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="58c3e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58c3e-117">PARAMETERS</span></span>

### <span data-ttu-id="58c3e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c3e-118">-DefaultProfile</span></span>
<span data-ttu-id="58c3e-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="58c3e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58c3e-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="58c3e-120">-IncludeDetail</span></span>
<span data-ttu-id="58c3e-121">Visualizzare altri dettagli sul Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="58c3e-121">Show more details about the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58c3e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="58c3e-122">-Name</span></span>
<span data-ttu-id="58c3e-123">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="58c3e-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c3e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c3e-124">-ResourceGroupName</span></span>
<span data-ttu-id="58c3e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58c3e-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c3e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58c3e-126">-ResourceId</span></span>
<span data-ttu-id="58c3e-127">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="58c3e-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58c3e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c3e-128">CommonParameters</span></span>
<span data-ttu-id="58c3e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c3e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c3e-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58c3e-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c3e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58c3e-131">INPUTS</span></span>

### <span data-ttu-id="58c3e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="58c3e-132">System.String</span></span>

## <span data-ttu-id="58c3e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58c3e-133">OUTPUTS</span></span>

### <span data-ttu-id="58c3e-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="58c3e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="58c3e-135">Note</span><span class="sxs-lookup"><span data-stu-id="58c3e-135">NOTES</span></span>

## <span data-ttu-id="58c3e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58c3e-136">RELATED LINKS</span></span>

[<span data-ttu-id="58c3e-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="58c3e-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="58c3e-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="58c3e-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="58c3e-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="58c3e-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

