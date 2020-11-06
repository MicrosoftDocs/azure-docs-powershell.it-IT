---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507555"
---
# <span data-ttu-id="1adbc-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1adbc-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="1adbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1adbc-102">SYNOPSIS</span></span>
<span data-ttu-id="1adbc-103">Ottiene un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1adbc-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1adbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1adbc-104">SYNTAX</span></span>

### <span data-ttu-id="1adbc-105">ListRegistriesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1adbc-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1adbc-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1adbc-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1adbc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1adbc-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1adbc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1adbc-108">DESCRIPTION</span></span>
<span data-ttu-id="1adbc-109">Il cmdlet Get-AzureRmContainerRegistry ottiene un registro dei contenitori specificato o tutti i registri contenitore in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1adbc-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="1adbc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1adbc-110">EXAMPLES</span></span>

### <span data-ttu-id="1adbc-111">Esempio 1: ottenere un registro di sistema contenitore specificato</span><span class="sxs-lookup"><span data-stu-id="1adbc-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="1adbc-112">Questo comando ottiene il registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="1adbc-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="1adbc-113">Esempio 2: ottenere tutti i registri dei contenitori in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1adbc-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="1adbc-114">Questo comando consente di ottenere tutti i registri contenitore in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1adbc-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="1adbc-115">Esempio 3: ottenere tutti i registri contenitore nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="1adbc-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

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

<span data-ttu-id="1adbc-116">Questo comando consente di ottenere tutti i registri contenitore nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1adbc-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="1adbc-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1adbc-117">PARAMETERS</span></span>

### <span data-ttu-id="1adbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1adbc-118">-DefaultProfile</span></span>
<span data-ttu-id="1adbc-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1adbc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1adbc-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="1adbc-120">-IncludeDetail</span></span>
<span data-ttu-id="1adbc-121">Visualizzare altri dettagli sul Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1adbc-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="1adbc-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1adbc-122">-Name</span></span>
<span data-ttu-id="1adbc-123">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1adbc-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="1adbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1adbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="1adbc-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1adbc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1adbc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1adbc-126">-ResourceId</span></span>
<span data-ttu-id="1adbc-127">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="1adbc-127">The container registry resource id</span></span>

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

### <span data-ttu-id="1adbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1adbc-128">CommonParameters</span></span>
<span data-ttu-id="1adbc-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1adbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1adbc-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1adbc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1adbc-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1adbc-131">INPUTS</span></span>

### <span data-ttu-id="1adbc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1adbc-132">System.String</span></span>

## <span data-ttu-id="1adbc-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1adbc-133">OUTPUTS</span></span>

### <span data-ttu-id="1adbc-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1adbc-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1adbc-135">Note</span><span class="sxs-lookup"><span data-stu-id="1adbc-135">NOTES</span></span>

## <span data-ttu-id="1adbc-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1adbc-136">RELATED LINKS</span></span>

[<span data-ttu-id="1adbc-137">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1adbc-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="1adbc-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1adbc-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="1adbc-139">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1adbc-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

