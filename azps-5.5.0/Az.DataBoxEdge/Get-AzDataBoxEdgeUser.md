---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: cc03472aa71665a8612e17bfce6365a255f929bd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194902"
---
# <span data-ttu-id="90499-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="90499-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="90499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90499-102">SYNOPSIS</span></span>
<span data-ttu-id="90499-103">Recupera gli utenti configurati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90499-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="90499-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90499-104">SYNTAX</span></span>

### <span data-ttu-id="90499-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90499-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90499-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90499-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90499-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="90499-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90499-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="90499-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="90499-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="90499-109">DESCRIPTION</span></span>
<span data-ttu-id="90499-110">Il **cmdlet Get-AzDataBoxEdgeUser** elenca gli utenti configurati per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="90499-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="90499-111">È possibile menzionare il nome nei parametri per ottenere informazioni dettagliate su un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="90499-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="90499-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90499-112">EXAMPLES</span></span>

### <span data-ttu-id="90499-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="90499-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="90499-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90499-114">PARAMETERS</span></span>

### <span data-ttu-id="90499-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90499-115">-DefaultProfile</span></span>
<span data-ttu-id="90499-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="90499-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90499-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="90499-117">-DeviceName</span></span>
<span data-ttu-id="90499-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="90499-118">Device Name</span></span>

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

### <span data-ttu-id="90499-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="90499-119">-DeviceObject</span></span>
<span data-ttu-id="90499-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="90499-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="90499-121">-Name</span><span class="sxs-lookup"><span data-stu-id="90499-121">-Name</span></span>
<span data-ttu-id="90499-122">Nome utente</span><span class="sxs-lookup"><span data-stu-id="90499-122">Username</span></span>

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

### <span data-ttu-id="90499-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90499-123">-ResourceGroupName</span></span>
<span data-ttu-id="90499-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="90499-124">Resource Group Name</span></span>

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

### <span data-ttu-id="90499-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90499-125">-ResourceId</span></span>
<span data-ttu-id="90499-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="90499-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="90499-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90499-127">CommonParameters</span></span>
<span data-ttu-id="90499-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90499-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90499-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90499-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90499-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="90499-130">INPUTS</span></span>

### <span data-ttu-id="90499-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="90499-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="90499-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90499-132">OUTPUTS</span></span>

### <span data-ttu-id="90499-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="90499-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="90499-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="90499-134">NOTES</span></span>

## <span data-ttu-id="90499-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90499-135">RELATED LINKS</span></span>
