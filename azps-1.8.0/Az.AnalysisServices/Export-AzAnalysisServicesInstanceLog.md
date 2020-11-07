---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 04a1c63ac2ae1b0db692f2bef4b4803a8acb744f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673697"
---
# <span data-ttu-id="4398f-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="4398f-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="4398f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4398f-102">SYNOPSIS</span></span>
<span data-ttu-id="4398f-103">Esporta un log da un'istanza del server di Analysis Services nell'ambiente attualmente connesso, come specificato nel comando Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4398f-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="4398f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4398f-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4398f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4398f-105">DESCRIPTION</span></span>
<span data-ttu-id="4398f-106">Il cmdlet Export-AzAnalysisServicesInstance Esporta il log da un'istanza di Azure Analysis Services server a file</span><span class="sxs-lookup"><span data-stu-id="4398f-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="4398f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4398f-107">EXAMPLES</span></span>

### <span data-ttu-id="4398f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4398f-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="4398f-109">Questo comando esporterà il log dal server "TestServer" nell'ambiente specificato nel comando Add-AzAnalysisServicesAccount e lo salverà in file specificato in OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="4398f-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="4398f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4398f-110">PARAMETERS</span></span>

### <span data-ttu-id="4398f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="4398f-111">-Force</span></span>
<span data-ttu-id="4398f-112">Sovrascrivere il file se esiste senza chiedere</span><span class="sxs-lookup"><span data-stu-id="4398f-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="4398f-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="4398f-113">-Instance</span></span>
<span data-ttu-id="4398f-114">Nome dell'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="4398f-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4398f-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="4398f-115">-OutputPath</span></span>
<span data-ttu-id="4398f-116">Percorso di output del file per esportare il log</span><span class="sxs-lookup"><span data-stu-id="4398f-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4398f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4398f-117">-PassThru</span></span>
<span data-ttu-id="4398f-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4398f-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4398f-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4398f-119">-Confirm</span></span>
<span data-ttu-id="4398f-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4398f-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4398f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4398f-121">-WhatIf</span></span>
<span data-ttu-id="4398f-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4398f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4398f-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4398f-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4398f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4398f-124">CommonParameters</span></span>
<span data-ttu-id="4398f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4398f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4398f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4398f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4398f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4398f-127">INPUTS</span></span>

### <span data-ttu-id="4398f-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4398f-128">None</span></span>

## <span data-ttu-id="4398f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4398f-129">OUTPUTS</span></span>

### <span data-ttu-id="4398f-130">System. void</span><span class="sxs-lookup"><span data-stu-id="4398f-130">System.Void</span></span>

## <span data-ttu-id="4398f-131">Note</span><span class="sxs-lookup"><span data-stu-id="4398f-131">NOTES</span></span>
<span data-ttu-id="4398f-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="4398f-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="4398f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4398f-133">RELATED LINKS</span></span>
