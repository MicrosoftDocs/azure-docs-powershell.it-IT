---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019010"
---
# <span data-ttu-id="dbc1b-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="dbc1b-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="dbc1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc1b-103">Ottiene gli utenti configurati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="dbc1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbc1b-104">SYNTAX</span></span>

### <span data-ttu-id="dbc1b-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dbc1b-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbc1b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbc1b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbc1b-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbc1b-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbc1b-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbc1b-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="dbc1b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbc1b-109">DESCRIPTION</span></span>
<span data-ttu-id="dbc1b-110">Il cmdlet **Get-AzStackEdgeUser** elenca gli utenti configurati per un dispositivo Edge in pila.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="dbc1b-111">Puoi menzionare il nome in parametri per ottenere informazioni dettagliate su un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="dbc1b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbc1b-112">EXAMPLES</span></span>

### <span data-ttu-id="dbc1b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbc1b-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="dbc1b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbc1b-114">PARAMETERS</span></span>

### <span data-ttu-id="dbc1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc1b-115">-DefaultProfile</span></span>
<span data-ttu-id="dbc1b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc1b-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="dbc1b-117">-DeviceName</span></span>
<span data-ttu-id="dbc1b-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="dbc1b-118">Device Name</span></span>

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

### <span data-ttu-id="dbc1b-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="dbc1b-119">-DeviceObject</span></span>
<span data-ttu-id="dbc1b-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="dbc1b-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="dbc1b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbc1b-121">-Name</span></span>
<span data-ttu-id="dbc1b-122">Username</span><span class="sxs-lookup"><span data-stu-id="dbc1b-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbc1b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc1b-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbc1b-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="dbc1b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dbc1b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbc1b-125">-ResourceId</span></span>
<span data-ttu-id="dbc1b-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dbc1b-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="dbc1b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc1b-127">CommonParameters</span></span>
<span data-ttu-id="dbc1b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc1b-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbc1b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc1b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbc1b-130">INPUTS</span></span>

### <span data-ttu-id="dbc1b-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="dbc1b-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="dbc1b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbc1b-132">OUTPUTS</span></span>

### <span data-ttu-id="dbc1b-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="dbc1b-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="dbc1b-134">Note</span><span class="sxs-lookup"><span data-stu-id="dbc1b-134">NOTES</span></span>

## <span data-ttu-id="dbc1b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbc1b-135">RELATED LINKS</span></span>
