---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 8845d9b5ac5dba0a2170e3184c866c39be29b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520124"
---
# <span data-ttu-id="2ee77-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="2ee77-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="2ee77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ee77-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee77-103">Ottenere i log di un'istanza di un contenitore in un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="2ee77-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ee77-104">SYNTAX</span></span>

### <span data-ttu-id="2ee77-105">GetContainerInstanceLogByNamesParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ee77-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee77-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="2ee77-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ee77-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="2ee77-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee77-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ee77-108">DESCRIPTION</span></span>
<span data-ttu-id="2ee77-109">Il cmdlet **Get-AzureRmContainerInstanceLog** recupera i log di un contenitore in un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="2ee77-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="2ee77-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ee77-110">EXAMPLES</span></span>

### <span data-ttu-id="2ee77-111">Esempio 1: ottenere il log della coda di un'istanza di contenitore</span><span class="sxs-lookup"><span data-stu-id="2ee77-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="2ee77-112">Ottenere il log dal `container1` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="2ee77-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="2ee77-113">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="2ee77-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="2ee77-114">Esempio 2: ottenere il log della coda di un'istanza del contenitore con lo stesso nome del gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="2ee77-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="2ee77-115">Ottenere il log dal `mycontainer` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="2ee77-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="2ee77-116">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="2ee77-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="2ee77-117">Esempio 3: ottenere la coda 2 righe di log di un'istanza di contenitore</span><span class="sxs-lookup"><span data-stu-id="2ee77-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="2ee77-118">Ottenere le righe della coda 2 del log dal `container1` gruppo contenitore `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="2ee77-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="2ee77-119">Esempio 4: ottenere il log della coda di un'istanza di un contenitore in un gruppo di contenitori con pipe in</span><span class="sxs-lookup"><span data-stu-id="2ee77-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="2ee77-120">Ottenere il log da `mycontainer` in pipe in un gruppo di contenitori `mycontainer` .</span><span class="sxs-lookup"><span data-stu-id="2ee77-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="2ee77-121">Per impostazione predefinita, verrà restituito il contenuto del log di 4 MB.</span><span class="sxs-lookup"><span data-stu-id="2ee77-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="2ee77-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ee77-122">PARAMETERS</span></span>

### <span data-ttu-id="2ee77-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee77-123">-ContainerGroupName</span></span>
<span data-ttu-id="2ee77-124">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="2ee77-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee77-125">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2ee77-125">-InputContainerGroup</span></span>
<span data-ttu-id="2ee77-126">Oggetto gruppo contenitore di input.</span><span class="sxs-lookup"><span data-stu-id="2ee77-126">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee77-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ee77-127">-Name</span></span>
<span data-ttu-id="2ee77-128">Nome dell'istanza del contenitore nel gruppo contenitore.</span><span class="sxs-lookup"><span data-stu-id="2ee77-128">The container instance name in the container group.</span></span>
<span data-ttu-id="2ee77-129">Impostazione predefinita: uguale al nome del gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="2ee77-129">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="2ee77-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee77-130">-ResourceGroupName</span></span>
<span data-ttu-id="2ee77-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ee77-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee77-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ee77-132">-ResourceId</span></span>
<span data-ttu-id="2ee77-133">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2ee77-133">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee77-134">-Coda</span><span class="sxs-lookup"><span data-stu-id="2ee77-134">-Tail</span></span>
<span data-ttu-id="2ee77-135">Numero di righe a cui eseguire il tail log.</span><span class="sxs-lookup"><span data-stu-id="2ee77-135">The number of lines to tail the log.</span></span>
<span data-ttu-id="2ee77-136">Se non si specifica, il cmdlet restituirà fino a un log di coda di 4 MB</span><span class="sxs-lookup"><span data-stu-id="2ee77-136">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee77-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee77-137">-DefaultProfile</span></span>
<span data-ttu-id="2ee77-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee77-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee77-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee77-139">CommonParameters</span></span>
<span data-ttu-id="2ee77-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee77-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee77-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee77-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee77-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ee77-142">INPUTS</span></span>

### <span data-ttu-id="2ee77-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2ee77-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="2ee77-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ee77-144">OUTPUTS</span></span>

### <span data-ttu-id="2ee77-145">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee77-145">System.String</span></span>

## <span data-ttu-id="2ee77-146">Note</span><span class="sxs-lookup"><span data-stu-id="2ee77-146">NOTES</span></span>

## <span data-ttu-id="2ee77-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ee77-147">RELATED LINKS</span></span>

