---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379119"
---
# <span data-ttu-id="c63e9-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="c63e9-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="c63e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c63e9-102">SYNOPSIS</span></span>
<span data-ttu-id="c63e9-103">Download della lettera di autorizzazione del documento per una porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="c63e9-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="c63e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c63e9-104">SYNTAX</span></span>

### <span data-ttu-id="c63e9-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c63e9-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63e9-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63e9-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c63e9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c63e9-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c63e9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c63e9-108">DESCRIPTION</span></span>
<span data-ttu-id="c63e9-109">New-AzExpressRoutePortLOA cmdlet Scarica il documento di una lettera di autorizzazione in formato PDF per una porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="c63e9-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="c63e9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c63e9-110">EXAMPLES</span></span>

### <span data-ttu-id="c63e9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c63e9-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="c63e9-112">Scaricare il documento di autorizzazione per la porta della route espressa "porta" e archiviarlo nel file "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="c63e9-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="c63e9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c63e9-113">PARAMETERS</span></span>

### <span data-ttu-id="c63e9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c63e9-114">-AsJob</span></span>
<span data-ttu-id="c63e9-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c63e9-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="c63e9-116">-CustomerName</span></span>
<span data-ttu-id="c63e9-117">Nome del cliente a cui è assegnata la porta di Route Express.</span><span class="sxs-lookup"><span data-stu-id="c63e9-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c63e9-118">-DefaultProfile</span></span>
<span data-ttu-id="c63e9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c63e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c63e9-120">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="c63e9-120">-Destination</span></span>
<span data-ttu-id="c63e9-121">FilePath di output in cui archiviare la lettera di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="c63e9-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="c63e9-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="c63e9-122">-ExpressRoutePort</span></span>
<span data-ttu-id="c63e9-123">Risorsa della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="c63e9-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-124">-ID</span><span class="sxs-lookup"><span data-stu-id="c63e9-124">-Id</span></span>
<span data-ttu-id="c63e9-125">ResourceId della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="c63e9-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c63e9-126">-PassThru</span></span>
<span data-ttu-id="c63e9-127">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c63e9-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="c63e9-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c63e9-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="c63e9-129">-PortName</span></span>
<span data-ttu-id="c63e9-130">Nome della porta Route espressa.</span><span class="sxs-lookup"><span data-stu-id="c63e9-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c63e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="c63e9-132">Nome del gruppo di risorse della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="c63e9-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c63e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c63e9-133">CommonParameters</span></span>
<span data-ttu-id="c63e9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c63e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c63e9-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c63e9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c63e9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c63e9-136">INPUTS</span></span>

### <span data-ttu-id="c63e9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c63e9-137">System.String</span></span>

## <span data-ttu-id="c63e9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c63e9-138">OUTPUTS</span></span>

### <span data-ttu-id="c63e9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c63e9-139">System.Boolean</span></span>

## <span data-ttu-id="c63e9-140">Note</span><span class="sxs-lookup"><span data-stu-id="c63e9-140">NOTES</span></span>

## <span data-ttu-id="c63e9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c63e9-141">RELATED LINKS</span></span>
