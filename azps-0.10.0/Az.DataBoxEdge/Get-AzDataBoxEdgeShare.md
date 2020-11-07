---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 9bcc19d29bf372aaa0b1c59e23f53e80edde4d17
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863285"
---
# <span data-ttu-id="a40ee-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a40ee-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="a40ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a40ee-102">SYNOPSIS</span></span>
<span data-ttu-id="a40ee-103">Ottiene le condivisioni disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a40ee-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="a40ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a40ee-104">SYNTAX</span></span>

### <span data-ttu-id="a40ee-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a40ee-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a40ee-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a40ee-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a40ee-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a40ee-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a40ee-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a40ee-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="a40ee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a40ee-109">DESCRIPTION</span></span>
<span data-ttu-id="a40ee-110">Il cmdlet **Get-AzDataBoxEdgeShare** ottiene le condivisioni disponibili per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="a40ee-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="a40ee-111">Se viene fornito il nome, otterrà il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="a40ee-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="a40ee-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a40ee-112">EXAMPLES</span></span>

### <span data-ttu-id="a40ee-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a40ee-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="a40ee-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a40ee-114">PARAMETERS</span></span>

### <span data-ttu-id="a40ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40ee-115">-DefaultProfile</span></span>
<span data-ttu-id="a40ee-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a40ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a40ee-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a40ee-117">-DeviceName</span></span>
<span data-ttu-id="a40ee-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a40ee-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40ee-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a40ee-119">-DeviceObject</span></span>
<span data-ttu-id="a40ee-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="a40ee-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a40ee-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a40ee-121">-Name</span></span>
<span data-ttu-id="a40ee-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a40ee-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40ee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40ee-123">-ResourceGroupName</span></span>
<span data-ttu-id="a40ee-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a40ee-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40ee-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a40ee-125">-ResourceId</span></span>
<span data-ttu-id="a40ee-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a40ee-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40ee-127">CommonParameters</span></span>
<span data-ttu-id="a40ee-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40ee-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a40ee-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40ee-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a40ee-130">INPUTS</span></span>

### <span data-ttu-id="a40ee-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a40ee-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a40ee-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a40ee-132">OUTPUTS</span></span>

### <span data-ttu-id="a40ee-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="a40ee-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="a40ee-134">Note</span><span class="sxs-lookup"><span data-stu-id="a40ee-134">NOTES</span></span>

## <span data-ttu-id="a40ee-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a40ee-135">RELATED LINKS</span></span>
