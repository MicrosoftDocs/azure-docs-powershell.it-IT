---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209643"
---
# <span data-ttu-id="98caa-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="98caa-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="98caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98caa-102">SYNOPSIS</span></span>
<span data-ttu-id="98caa-103">Creare un oggetto in memoria per DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="98caa-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="98caa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98caa-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="98caa-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98caa-105">DESCRIPTION</span></span>
<span data-ttu-id="98caa-106">Creare un oggetto in memoria per DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="98caa-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="98caa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98caa-107">EXAMPLES</span></span>

### <span data-ttu-id="98caa-108">Esempio 1: Creare un oggetto DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="98caa-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="98caa-109">Creare un oggetto DigitalTwinsIdentityObject in base a ID e percorso</span><span class="sxs-lookup"><span data-stu-id="98caa-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="98caa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98caa-110">PARAMETERS</span></span>

### <span data-ttu-id="98caa-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="98caa-111">-EndpointName</span></span>
<span data-ttu-id="98caa-112">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="98caa-112">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98caa-113">-Id</span><span class="sxs-lookup"><span data-stu-id="98caa-113">-Id</span></span>
<span data-ttu-id="98caa-114">Percorso di identità della risorsa.</span><span class="sxs-lookup"><span data-stu-id="98caa-114">Resource identity path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98caa-115">-Location</span><span class="sxs-lookup"><span data-stu-id="98caa-115">-Location</span></span>
<span data-ttu-id="98caa-116">Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="98caa-116">Location of DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98caa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98caa-117">-ResourceGroupName</span></span>
<span data-ttu-id="98caa-118">Nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="98caa-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98caa-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="98caa-119">-ResourceName</span></span>
<span data-ttu-id="98caa-120">Nome di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="98caa-120">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98caa-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98caa-121">-SubscriptionId</span></span>
<span data-ttu-id="98caa-122">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="98caa-122">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98caa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98caa-123">CommonParameters</span></span>
<span data-ttu-id="98caa-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98caa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98caa-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98caa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98caa-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="98caa-126">INPUTS</span></span>

## <span data-ttu-id="98caa-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98caa-127">OUTPUTS</span></span>

### <span data-ttu-id="98caa-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="98caa-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="98caa-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="98caa-129">NOTES</span></span>

<span data-ttu-id="98caa-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="98caa-130">ALIASES</span></span>

## <span data-ttu-id="98caa-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98caa-131">RELATED LINKS</span></span>

