---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200406"
---
# <span data-ttu-id="ddc48-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ddc48-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="ddc48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ddc48-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc48-103">Ottiene le condivisioni disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddc48-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="ddc48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ddc48-104">SYNTAX</span></span>

### <span data-ttu-id="ddc48-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ddc48-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddc48-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc48-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddc48-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc48-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddc48-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ddc48-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="ddc48-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddc48-109">DESCRIPTION</span></span>
<span data-ttu-id="ddc48-110">Il cmdlet **Get-AzStackEdgeShare** ottiene le condivisioni disponibili per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="ddc48-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="ddc48-111">Se viene fornito il nome, otterrà il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="ddc48-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="ddc48-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ddc48-112">EXAMPLES</span></span>

### <span data-ttu-id="ddc48-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ddc48-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="ddc48-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ddc48-114">PARAMETERS</span></span>

### <span data-ttu-id="ddc48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc48-115">-DefaultProfile</span></span>
<span data-ttu-id="ddc48-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc48-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ddc48-117">-DeviceName</span></span>
<span data-ttu-id="ddc48-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="ddc48-118">Device Name</span></span>

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

### <span data-ttu-id="ddc48-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="ddc48-119">-DeviceObject</span></span>
<span data-ttu-id="ddc48-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="ddc48-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc48-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddc48-121">-Name</span></span>
<span data-ttu-id="ddc48-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="ddc48-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc48-123">-ResourceGroupName</span></span>
<span data-ttu-id="ddc48-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ddc48-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ddc48-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc48-125">-ResourceId</span></span>
<span data-ttu-id="ddc48-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc48-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddc48-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc48-127">CommonParameters</span></span>
<span data-ttu-id="ddc48-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddc48-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc48-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddc48-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc48-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ddc48-130">INPUTS</span></span>

### <span data-ttu-id="ddc48-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="ddc48-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="ddc48-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ddc48-132">OUTPUTS</span></span>

### <span data-ttu-id="ddc48-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="ddc48-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="ddc48-134">Note</span><span class="sxs-lookup"><span data-stu-id="ddc48-134">NOTES</span></span>

## <span data-ttu-id="ddc48-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ddc48-135">RELATED LINKS</span></span>
