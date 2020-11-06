---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: b2107a667fe3d00ec0b6e9180b2edc99e864445c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507559"
---
# <span data-ttu-id="e6211-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e6211-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="e6211-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6211-102">SYNOPSIS</span></span>
<span data-ttu-id="e6211-103">Ottiene i gruppi di contenitori.</span><span class="sxs-lookup"><span data-stu-id="e6211-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6211-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6211-104">SYNTAX</span></span>

### <span data-ttu-id="e6211-105">ListContainerGroupParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6211-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6211-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="e6211-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6211-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="e6211-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6211-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6211-108">DESCRIPTION</span></span>
<span data-ttu-id="e6211-109">Il cmdlet **Get-AzureRmContainerGroup** ottiene un gruppo di contenitori specificato o tutti i gruppi di contenitori in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e6211-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="e6211-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6211-110">EXAMPLES</span></span>

### <span data-ttu-id="e6211-111">Esempio 1: ottiene un gruppo di contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="e6211-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6211-112">Il comando ottiene il gruppo di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="e6211-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="e6211-113">Esempio 2: ottiene i gruppi di contenitori in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e6211-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="e6211-114">Il comando ottiene i gruppi di contenitori nel gruppo di risorse `demo` .</span><span class="sxs-lookup"><span data-stu-id="e6211-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="e6211-115">Esempio 3: ottiene i gruppi di contenitori nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="e6211-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="e6211-116">Il comando ottiene i gruppi di contenitori nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e6211-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="e6211-117">Esempio 4: recupera i gruppi di contenitori usando l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e6211-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="e6211-118">Il comando ottiene il gruppo contenitore con l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e6211-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="e6211-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6211-119">PARAMETERS</span></span>

### <span data-ttu-id="e6211-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6211-120">-DefaultProfile</span></span>
<span data-ttu-id="e6211-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6211-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6211-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6211-122">-Name</span></span>
<span data-ttu-id="e6211-123">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="e6211-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6211-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6211-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6211-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e6211-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6211-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6211-126">-ResourceId</span></span>
<span data-ttu-id="e6211-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e6211-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6211-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6211-128">CommonParameters</span></span>
<span data-ttu-id="e6211-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6211-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6211-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6211-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6211-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6211-131">INPUTS</span></span>

### <span data-ttu-id="e6211-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e6211-132">System.String</span></span>

## <span data-ttu-id="e6211-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6211-133">OUTPUTS</span></span>

### <span data-ttu-id="e6211-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="e6211-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="e6211-135">Note</span><span class="sxs-lookup"><span data-stu-id="e6211-135">NOTES</span></span>

## <span data-ttu-id="e6211-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6211-136">RELATED LINKS</span></span>
