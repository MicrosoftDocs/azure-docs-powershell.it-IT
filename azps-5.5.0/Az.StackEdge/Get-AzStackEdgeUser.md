---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183222"
---
# <span data-ttu-id="2c304-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="2c304-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="2c304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c304-102">SYNOPSIS</span></span>
<span data-ttu-id="2c304-103">Recupera gli utenti configurati per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c304-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="2c304-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c304-104">SYNTAX</span></span>

### <span data-ttu-id="2c304-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c304-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c304-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c304-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c304-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c304-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c304-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c304-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="2c304-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2c304-109">DESCRIPTION</span></span>
<span data-ttu-id="2c304-110">Il **cmdlet Get-AzStackEdgeUser** elenca gli utenti configurati per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="2c304-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="2c304-111">È possibile menzionare il nome nei parametri per ottenere informazioni dettagliate su un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="2c304-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="2c304-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c304-112">EXAMPLES</span></span>

### <span data-ttu-id="2c304-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2c304-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="2c304-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c304-114">PARAMETERS</span></span>

### <span data-ttu-id="2c304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c304-115">-DefaultProfile</span></span>
<span data-ttu-id="2c304-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c304-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c304-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2c304-117">-DeviceName</span></span>
<span data-ttu-id="2c304-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="2c304-118">Device Name</span></span>

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

### <span data-ttu-id="2c304-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="2c304-119">-DeviceObject</span></span>
<span data-ttu-id="2c304-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="2c304-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="2c304-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2c304-121">-Name</span></span>
<span data-ttu-id="2c304-122">Nome utente</span><span class="sxs-lookup"><span data-stu-id="2c304-122">Username</span></span>

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

### <span data-ttu-id="2c304-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c304-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c304-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2c304-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2c304-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c304-125">-ResourceId</span></span>
<span data-ttu-id="2c304-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c304-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="2c304-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c304-127">CommonParameters</span></span>
<span data-ttu-id="2c304-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c304-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c304-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c304-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c304-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="2c304-130">INPUTS</span></span>

### <span data-ttu-id="2c304-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2c304-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="2c304-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c304-132">OUTPUTS</span></span>

### <span data-ttu-id="2c304-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="2c304-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="2c304-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="2c304-134">NOTES</span></span>

## <span data-ttu-id="2c304-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c304-135">RELATED LINKS</span></span>
