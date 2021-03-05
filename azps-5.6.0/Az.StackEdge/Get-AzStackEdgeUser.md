---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 9d06873954e6a6880965781d2004d8b7b0c35bb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977645"
---
# <span data-ttu-id="114c0-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="114c0-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="114c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="114c0-102">SYNOPSIS</span></span>
<span data-ttu-id="114c0-103">Recupera gli utenti configurati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="114c0-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="114c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="114c0-104">SYNTAX</span></span>

### <span data-ttu-id="114c0-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="114c0-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="114c0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="114c0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="114c0-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="114c0-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="114c0-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="114c0-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="114c0-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="114c0-109">DESCRIPTION</span></span>
<span data-ttu-id="114c0-110">Il **cmdlet Get-AzStackEdgeUser** elenca gli utenti configurati per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="114c0-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="114c0-111">È possibile menzionare il nome nei parametri per ottenere informazioni dettagliate su un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="114c0-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="114c0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="114c0-112">EXAMPLES</span></span>

### <span data-ttu-id="114c0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="114c0-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="114c0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="114c0-114">PARAMETERS</span></span>

### <span data-ttu-id="114c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114c0-115">-DefaultProfile</span></span>
<span data-ttu-id="114c0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="114c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="114c0-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="114c0-117">-DeviceName</span></span>
<span data-ttu-id="114c0-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="114c0-118">Device Name</span></span>

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

### <span data-ttu-id="114c0-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="114c0-119">-DeviceObject</span></span>
<span data-ttu-id="114c0-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="114c0-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="114c0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="114c0-121">-Name</span></span>
<span data-ttu-id="114c0-122">Nome utente</span><span class="sxs-lookup"><span data-stu-id="114c0-122">Username</span></span>

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

### <span data-ttu-id="114c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="114c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="114c0-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="114c0-124">Resource Group Name</span></span>

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

### <span data-ttu-id="114c0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="114c0-125">-ResourceId</span></span>
<span data-ttu-id="114c0-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="114c0-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="114c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114c0-127">CommonParameters</span></span>
<span data-ttu-id="114c0-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114c0-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="114c0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114c0-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="114c0-130">INPUTS</span></span>

### <span data-ttu-id="114c0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="114c0-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="114c0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="114c0-132">OUTPUTS</span></span>

### <span data-ttu-id="114c0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="114c0-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="114c0-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="114c0-134">NOTES</span></span>

## <span data-ttu-id="114c0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="114c0-135">RELATED LINKS</span></span>
