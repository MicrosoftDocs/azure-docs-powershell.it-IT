---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019009"
---
# <span data-ttu-id="d9be2-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d9be2-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="d9be2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9be2-102">SYNOPSIS</span></span>
<span data-ttu-id="d9be2-103">Ottiene i contenitori per un account di archiviazione perimetrale in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9be2-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="d9be2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9be2-104">SYNTAX</span></span>

### <span data-ttu-id="d9be2-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9be2-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9be2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9be2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9be2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9be2-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9be2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9be2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="d9be2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9be2-109">DESCRIPTION</span></span>
<span data-ttu-id="d9be2-110">Il cmdlet **Get-AzStackEdgeStorageContainer** ottiene il contenitore di archiviazione per un account di archiviazione perimetrale in un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="d9be2-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="d9be2-111">Puoi specificare il nome come parametro nel cmdlet per recuperare i dettagli di un contenitore di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="d9be2-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="d9be2-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9be2-112">EXAMPLES</span></span>

### <span data-ttu-id="d9be2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9be2-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d9be2-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d9be2-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d9be2-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d9be2-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="d9be2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9be2-116">PARAMETERS</span></span>

### <span data-ttu-id="d9be2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9be2-117">-DefaultProfile</span></span>
<span data-ttu-id="d9be2-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9be2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9be2-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d9be2-119">-DeviceName</span></span>
<span data-ttu-id="d9be2-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="d9be2-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be2-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d9be2-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d9be2-122">Fornisci il nome di EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="d9be2-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be2-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="d9be2-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="d9be2-124">Fornisci l'oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="d9be2-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9be2-125">-Name</span></span>
<span data-ttu-id="d9be2-126">Nome del EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d9be2-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9be2-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9be2-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d9be2-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9be2-129">-ResourceId</span></span>
<span data-ttu-id="d9be2-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9be2-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9be2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9be2-131">CommonParameters</span></span>
<span data-ttu-id="d9be2-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9be2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9be2-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9be2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9be2-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9be2-134">INPUTS</span></span>

### <span data-ttu-id="d9be2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d9be2-135">System.String</span></span>

### <span data-ttu-id="d9be2-136">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d9be2-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="d9be2-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9be2-137">OUTPUTS</span></span>

### <span data-ttu-id="d9be2-138">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d9be2-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="d9be2-139">Note</span><span class="sxs-lookup"><span data-stu-id="d9be2-139">NOTES</span></span>

## <span data-ttu-id="d9be2-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9be2-140">RELATED LINKS</span></span>
