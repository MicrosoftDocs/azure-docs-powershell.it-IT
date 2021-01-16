---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.DigitalTwins/new-AzDigitalTwinsDigitalTwinsIdentityObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsDigitalTwinsIdentityObject.md
ms.openlocfilehash: c78ad67e884eeac1cc6f4b589fd15e0493ee738a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475301"
---
# <span data-ttu-id="71f72-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="71f72-101">New-AzDigitalTwinsDigitalTwinsIdentityObject</span></span>

## <span data-ttu-id="71f72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71f72-102">SYNOPSIS</span></span>
<span data-ttu-id="71f72-103">Creare un oggetto in memoria per DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="71f72-103">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="71f72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71f72-104">SYNTAX</span></span>

```
New-AzDigitalTwinsDigitalTwinsIdentityObject [-EndpointName <String>] [-Id <String>] [-Location <String>]
 [-ResourceGroupName <String>] [-ResourceName <String>] [-SubscriptionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="71f72-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71f72-105">DESCRIPTION</span></span>
<span data-ttu-id="71f72-106">Creare un oggetto in memoria per DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="71f72-106">Create a in-memory object for DigitalTwinsIdentity</span></span>

## <span data-ttu-id="71f72-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71f72-107">EXAMPLES</span></span>

### <span data-ttu-id="71f72-108">Esempio 1: creare un DigitalTwinsIdentityObject</span><span class="sxs-lookup"><span data-stu-id="71f72-108">Example 1: Create A DigitalTwinsIdentityObject</span></span>
```powershell
PS C:\> New-AzDigitalTwinsDigitalTwinsIdentityObject -Id '************' -Location eastus

EndpointName Location ResourceGroupName ResourceName SubscriptionId
------------ -------- ----------------- ------------ --------------
             eastus
```

<span data-ttu-id="71f72-109">Creare un DigitalTwinsIdentityObject in base all'ID e alla posizione</span><span class="sxs-lookup"><span data-stu-id="71f72-109">Create A DigitalTwinsIdentityObject by Id and location</span></span>

## <span data-ttu-id="71f72-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71f72-110">PARAMETERS</span></span>

### <span data-ttu-id="71f72-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="71f72-111">-EndpointName</span></span>
<span data-ttu-id="71f72-112">Nome della risorsa endpoint.</span><span class="sxs-lookup"><span data-stu-id="71f72-112">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="71f72-113">-ID</span><span class="sxs-lookup"><span data-stu-id="71f72-113">-Id</span></span>
<span data-ttu-id="71f72-114">Percorso identità risorse.</span><span class="sxs-lookup"><span data-stu-id="71f72-114">Resource identity path.</span></span>

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

### <span data-ttu-id="71f72-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="71f72-115">-Location</span></span>
<span data-ttu-id="71f72-116">Posizione di DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71f72-116">Location of DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="71f72-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f72-117">-ResourceGroupName</span></span>
<span data-ttu-id="71f72-118">Il nome del gruppo di risorse che contiene DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71f72-118">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="71f72-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="71f72-119">-ResourceName</span></span>
<span data-ttu-id="71f72-120">Il nome del DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="71f72-120">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="71f72-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71f72-121">-SubscriptionId</span></span>
<span data-ttu-id="71f72-122">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="71f72-122">The subscription identifier.</span></span>

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

### <span data-ttu-id="71f72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f72-123">CommonParameters</span></span>
<span data-ttu-id="71f72-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f72-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71f72-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f72-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71f72-126">INPUTS</span></span>

## <span data-ttu-id="71f72-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71f72-127">OUTPUTS</span></span>

### <span data-ttu-id="71f72-128">Microsoft. Azure. PowerShell. Cmdlets. DigitalTwins. Models. DigitalTwinsIdentity</span><span class="sxs-lookup"><span data-stu-id="71f72-128">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.DigitalTwinsIdentity</span></span>

## <span data-ttu-id="71f72-129">Note</span><span class="sxs-lookup"><span data-stu-id="71f72-129">NOTES</span></span>

<span data-ttu-id="71f72-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="71f72-130">ALIASES</span></span>

## <span data-ttu-id="71f72-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71f72-131">RELATED LINKS</span></span>

