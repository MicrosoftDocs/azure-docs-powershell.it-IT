---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 0ab290934a956282a16d9e2321b2c5ed948f33af
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863270"
---
# <span data-ttu-id="e6b8f-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e6b8f-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="e6b8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b8f-103">Ottiene gli utenti configurati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="e6b8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6b8f-104">SYNTAX</span></span>

### <span data-ttu-id="e6b8f-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6b8f-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b8f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b8f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b8f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b8f-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b8f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b8f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e6b8f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6b8f-109">DESCRIPTION</span></span>
<span data-ttu-id="e6b8f-110">Il cmdlet **Get-AzDataBoxEdgeUser** elenca gli utenti configurati per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="e6b8f-111">Puoi menzionare il nome in parametri per ottenere informazioni dettagliate su un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="e6b8f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6b8f-112">EXAMPLES</span></span>

### <span data-ttu-id="e6b8f-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6b8f-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="e6b8f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6b8f-114">PARAMETERS</span></span>

### <span data-ttu-id="e6b8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b8f-115">-DefaultProfile</span></span>
<span data-ttu-id="e6b8f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b8f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e6b8f-117">-DeviceName</span></span>
<span data-ttu-id="e6b8f-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="e6b8f-118">Device Name</span></span>

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

### <span data-ttu-id="e6b8f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e6b8f-119">-DeviceObject</span></span>
<span data-ttu-id="e6b8f-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="e6b8f-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e6b8f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6b8f-121">-Name</span></span>
<span data-ttu-id="e6b8f-122">Username</span><span class="sxs-lookup"><span data-stu-id="e6b8f-122">Username</span></span>

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

### <span data-ttu-id="e6b8f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6b8f-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6b8f-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e6b8f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e6b8f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b8f-125">-ResourceId</span></span>
<span data-ttu-id="e6b8f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6b8f-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="e6b8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b8f-127">CommonParameters</span></span>
<span data-ttu-id="e6b8f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b8f-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b8f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6b8f-130">INPUTS</span></span>

### <span data-ttu-id="e6b8f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e6b8f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e6b8f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6b8f-132">OUTPUTS</span></span>

### <span data-ttu-id="e6b8f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e6b8f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="e6b8f-134">Note</span><span class="sxs-lookup"><span data-stu-id="e6b8f-134">NOTES</span></span>

## <span data-ttu-id="e6b8f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6b8f-135">RELATED LINKS</span></span>
