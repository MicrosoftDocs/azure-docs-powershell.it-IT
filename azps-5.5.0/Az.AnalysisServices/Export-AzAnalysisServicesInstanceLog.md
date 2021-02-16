---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199767"
---
# <span data-ttu-id="8cbc4-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="8cbc4-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="8cbc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbc4-103">Esporta un log da un'istanza del server analysis services nell'ambiente attualmente connesso come specificato nel comando Add-AzAnalysisServicesAccount></span><span class="sxs-lookup"><span data-stu-id="8cbc4-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="8cbc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cbc4-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cbc4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cbc4-105">DESCRIPTION</span></span>
<span data-ttu-id="8cbc4-106">Il cmdlet Export-AzAnalysisServicesInstance esporta il log da un'istanza del server di Azure Analysis Services in file</span><span class="sxs-lookup"><span data-stu-id="8cbc4-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="8cbc4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cbc4-107">EXAMPLES</span></span>

### <span data-ttu-id="8cbc4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cbc4-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="8cbc4-109">Questo comando esporta il log dal server 'testserver' nell'ambiente specificato nel comando Add-AzAnalysisServicesAccount e lo salva nel file specificato in OutputPath 'C:\path\to\log\testserver.log'</span><span class="sxs-lookup"><span data-stu-id="8cbc4-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="8cbc4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cbc4-110">PARAMETERS</span></span>

### <span data-ttu-id="8cbc4-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8cbc4-111">-Force</span></span>
<span data-ttu-id="8cbc4-112">Sovrascrivere il file, se esistente senza chiedere</span><span class="sxs-lookup"><span data-stu-id="8cbc4-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="8cbc4-113">-Instance</span><span class="sxs-lookup"><span data-stu-id="8cbc4-113">-Instance</span></span>
<span data-ttu-id="8cbc4-114">Nome dell'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="8cbc4-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="8cbc4-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="8cbc4-115">-OutputPath</span></span>
<span data-ttu-id="8cbc4-116">Percorso di output del file da esportare</span><span class="sxs-lookup"><span data-stu-id="8cbc4-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="8cbc4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8cbc4-117">-PassThru</span></span>
<span data-ttu-id="8cbc4-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8cbc4-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8cbc4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cbc4-119">-Confirm</span></span>
<span data-ttu-id="8cbc4-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cbc4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbc4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbc4-121">-WhatIf</span></span>
<span data-ttu-id="8cbc4-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cbc4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cbc4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cbc4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbc4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbc4-124">CommonParameters</span></span>
<span data-ttu-id="8cbc4-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbc4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbc4-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbc4-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbc4-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cbc4-127">INPUTS</span></span>

### <span data-ttu-id="8cbc4-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8cbc4-128">None</span></span>

## <span data-ttu-id="8cbc4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cbc4-129">OUTPUTS</span></span>

### <span data-ttu-id="8cbc4-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="8cbc4-130">System.Void</span></span>

## <span data-ttu-id="8cbc4-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cbc4-131">NOTES</span></span>
<span data-ttu-id="8cbc4-132">Alias: Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="8cbc4-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="8cbc4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cbc4-133">RELATED LINKS</span></span>
