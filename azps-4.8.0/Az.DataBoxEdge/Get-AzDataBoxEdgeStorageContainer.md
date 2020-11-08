---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3f7ebc42efc2ad5ba73079fd2774614b941f432b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190314"
---
# <span data-ttu-id="8b3ae-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b3ae-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="8b3ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b3ae-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3ae-103">Ottiene i contenitori per un account di archiviazione perimetrale in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8b3ae-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="8b3ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b3ae-104">SYNTAX</span></span>

### <span data-ttu-id="8b3ae-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b3ae-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b3ae-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b3ae-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b3ae-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b3ae-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b3ae-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b3ae-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="8b3ae-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b3ae-109">DESCRIPTION</span></span>
<span data-ttu-id="8b3ae-110">Il cmdlet **Get-AzDataBoxEdgeStorageContainer** ottiene il contenitore di archiviazione per un account di archiviazione Edge in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="8b3ae-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="8b3ae-111">Puoi specificare il nome come parametro nel cmdlet per recuperare i dettagli di un contenitore di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="8b3ae-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="8b3ae-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b3ae-112">EXAMPLES</span></span>

### <span data-ttu-id="8b3ae-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b3ae-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="8b3ae-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b3ae-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="8b3ae-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8b3ae-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="8b3ae-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b3ae-116">PARAMETERS</span></span>

### <span data-ttu-id="8b3ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3ae-117">-DefaultProfile</span></span>
<span data-ttu-id="8b3ae-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b3ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b3ae-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8b3ae-119">-DeviceName</span></span>
<span data-ttu-id="8b3ae-120">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="8b3ae-120">Device Name</span></span>

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

### <span data-ttu-id="8b3ae-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b3ae-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="8b3ae-122">Fornisci il nome di EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="8b3ae-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="8b3ae-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="8b3ae-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="8b3ae-124">Fornisci l'oggetto EdgeStorageAccount esistente</span><span class="sxs-lookup"><span data-stu-id="8b3ae-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b3ae-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b3ae-125">-Name</span></span>
<span data-ttu-id="8b3ae-126">Nome del EdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b3ae-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="8b3ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b3ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b3ae-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8b3ae-128">Resource Group Name</span></span>

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

### <span data-ttu-id="8b3ae-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b3ae-129">-ResourceId</span></span>
<span data-ttu-id="8b3ae-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b3ae-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="8b3ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3ae-131">CommonParameters</span></span>
<span data-ttu-id="8b3ae-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b3ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3ae-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b3ae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3ae-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b3ae-134">INPUTS</span></span>

### <span data-ttu-id="8b3ae-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8b3ae-135">System.String</span></span>

### <span data-ttu-id="8b3ae-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b3ae-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="8b3ae-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b3ae-137">OUTPUTS</span></span>

### <span data-ttu-id="8b3ae-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b3ae-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="8b3ae-139">Note</span><span class="sxs-lookup"><span data-stu-id="8b3ae-139">NOTES</span></span>

## <span data-ttu-id="8b3ae-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b3ae-140">RELATED LINKS</span></span>
