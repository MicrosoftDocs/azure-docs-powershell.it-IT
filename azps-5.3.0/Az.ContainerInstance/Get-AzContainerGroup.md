---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 2dadcac9f0b537a52a0a7270b7d20fc08e80461c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477588"
---
# <span data-ttu-id="a4b24-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a4b24-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="a4b24-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4b24-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b24-103">Ottiene i gruppi di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a4b24-103">Gets container groups.</span></span>

## <span data-ttu-id="a4b24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4b24-104">SYNTAX</span></span>

### <span data-ttu-id="a4b24-105">ListContainerGroupParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4b24-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b24-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="a4b24-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b24-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a4b24-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4b24-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4b24-108">DESCRIPTION</span></span>
<span data-ttu-id="a4b24-109">Il cmdlet **Get-AzContainerGroup** ottiene un gruppo di contenitori specificato o tutti i gruppi di contenitori in un gruppo di risorse o nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a4b24-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="a4b24-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4b24-110">EXAMPLES</span></span>

### <span data-ttu-id="a4b24-111">Esempio 1: ottiene un gruppo di contenitori specificato</span><span class="sxs-lookup"><span data-stu-id="a4b24-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

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

<span data-ttu-id="a4b24-112">Il comando ottiene il gruppo di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="a4b24-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="a4b24-113">Esempio 2: ottiene i gruppi di contenitori in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a4b24-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="a4b24-114">Il comando ottiene i gruppi di contenitori nel gruppo di risorse `demo` .</span><span class="sxs-lookup"><span data-stu-id="a4b24-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="a4b24-115">Esempio 3: ottiene i gruppi di contenitori nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="a4b24-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="a4b24-116">Il comando ottiene i gruppi di contenitori nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="a4b24-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="a4b24-117">Esempio 4: recupera i gruppi di contenitori usando l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4b24-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

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

<span data-ttu-id="a4b24-118">Il comando ottiene il gruppo contenitore con l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4b24-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="a4b24-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4b24-119">PARAMETERS</span></span>

### <span data-ttu-id="a4b24-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b24-120">-DefaultProfile</span></span>
<span data-ttu-id="a4b24-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b24-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b24-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4b24-122">-Name</span></span>
<span data-ttu-id="a4b24-123">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="a4b24-123">The container group Name.</span></span>

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

### <span data-ttu-id="a4b24-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b24-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4b24-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4b24-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="a4b24-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b24-126">-ResourceId</span></span>
<span data-ttu-id="a4b24-127">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4b24-127">The resource id.</span></span>

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

### <span data-ttu-id="a4b24-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b24-128">CommonParameters</span></span>
<span data-ttu-id="a4b24-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b24-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b24-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b24-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b24-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4b24-131">INPUTS</span></span>

### <span data-ttu-id="a4b24-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b24-132">System.String</span></span>

## <span data-ttu-id="a4b24-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4b24-133">OUTPUTS</span></span>

### <span data-ttu-id="a4b24-134">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="a4b24-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="a4b24-135">Note</span><span class="sxs-lookup"><span data-stu-id="a4b24-135">NOTES</span></span>

## <span data-ttu-id="a4b24-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4b24-136">RELATED LINKS</span></span>
