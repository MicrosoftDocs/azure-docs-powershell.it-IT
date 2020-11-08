---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191796"
---
# <span data-ttu-id="fa5a9-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fa5a9-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="fa5a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5a9-103">Recupera i ruoli disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa5a9-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="fa5a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa5a9-104">SYNTAX</span></span>

### <span data-ttu-id="fa5a9-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa5a9-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5a9-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa5a9-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5a9-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa5a9-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa5a9-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa5a9-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="fa5a9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa5a9-109">DESCRIPTION</span></span>
<span data-ttu-id="fa5a9-110">Il cmdlet **Get-AzStackEdgeRole** recupera i ruoli disponibili per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="fa5a9-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="fa5a9-111">Puoi menzionare il parametro Name per ottenere i dettagli di un ruolo specifico.</span><span class="sxs-lookup"><span data-stu-id="fa5a9-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="fa5a9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa5a9-112">EXAMPLES</span></span>

### <span data-ttu-id="fa5a9-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa5a9-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="fa5a9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa5a9-114">PARAMETERS</span></span>

### <span data-ttu-id="fa5a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5a9-115">-DefaultProfile</span></span>
<span data-ttu-id="fa5a9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa5a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa5a9-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fa5a9-117">-DeviceName</span></span>
<span data-ttu-id="fa5a9-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa5a9-118">Device Name</span></span>

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

### <span data-ttu-id="fa5a9-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fa5a9-119">-DeviceObject</span></span>
<span data-ttu-id="fa5a9-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="fa5a9-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="fa5a9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa5a9-121">-Name</span></span>
<span data-ttu-id="fa5a9-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="fa5a9-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa5a9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5a9-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa5a9-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="fa5a9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="fa5a9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa5a9-125">-ResourceId</span></span>
<span data-ttu-id="fa5a9-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa5a9-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="fa5a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5a9-127">CommonParameters</span></span>
<span data-ttu-id="fa5a9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa5a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5a9-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa5a9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5a9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa5a9-130">INPUTS</span></span>

### <span data-ttu-id="fa5a9-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fa5a9-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="fa5a9-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa5a9-132">OUTPUTS</span></span>

### <span data-ttu-id="fa5a9-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="fa5a9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="fa5a9-134">Note</span><span class="sxs-lookup"><span data-stu-id="fa5a9-134">NOTES</span></span>

## <span data-ttu-id="fa5a9-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa5a9-135">RELATED LINKS</span></span>
