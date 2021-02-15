---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207290"
---
# <span data-ttu-id="5bb1c-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="5bb1c-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="5bb1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb1c-103">Esporta l'oggetto definizione del servizio Web come stringa in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="5bb1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5bb1c-104">SYNTAX</span></span>

### <span data-ttu-id="5bb1c-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="5bb1c-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bb1c-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="5bb1c-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bb1c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5bb1c-107">DESCRIPTION</span></span>
<span data-ttu-id="5bb1c-108">Esporta l'oggetto definizione per il servizio Web specificato come stringa in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="5bb1c-109">È possibile restituire la stringa immediatamente o salvarla in un file.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="5bb1c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5bb1c-110">EXAMPLES</span></span>

### <span data-ttu-id="5bb1c-111">Esempio 1: Esportare come stringa</span><span class="sxs-lookup"><span data-stu-id="5bb1c-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="5bb1c-112">Esempio 2: Esportare in un file</span><span class="sxs-lookup"><span data-stu-id="5bb1c-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="5bb1c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5bb1c-113">PARAMETERS</span></span>

### <span data-ttu-id="5bb1c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb1c-114">-DefaultProfile</span></span>
<span data-ttu-id="5bb1c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5bb1c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bb1c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5bb1c-116">-Force</span></span>
<span data-ttu-id="5bb1c-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5bb1c-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5bb1c-118">-OutputFile</span></span>
<span data-ttu-id="5bb1c-119">Percorso file per la definizione esportata.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb1c-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="5bb1c-120">-ToJsonString</span></span>
<span data-ttu-id="5bb1c-121">Specifica che la definizione verrà esportata come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb1c-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="5bb1c-122">-WebService</span></span>
<span data-ttu-id="5bb1c-123">Oggetto definizione del servizio Web da esportare.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb1c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bb1c-124">-Confirm</span></span>
<span data-ttu-id="5bb1c-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bb1c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb1c-126">-WhatIf</span></span>
<span data-ttu-id="5bb1c-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bb1c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bb1c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb1c-129">CommonParameters</span></span>
<span data-ttu-id="5bb1c-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bb1c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb1c-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bb1c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb1c-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="5bb1c-132">INPUTS</span></span>

### <span data-ttu-id="5bb1c-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="5bb1c-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="5bb1c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5bb1c-134">OUTPUTS</span></span>

### <span data-ttu-id="5bb1c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5bb1c-135">System.String</span></span>

## <span data-ttu-id="5bb1c-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="5bb1c-136">NOTES</span></span>
<span data-ttu-id="5bb1c-137">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="5bb1c-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="5bb1c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5bb1c-138">RELATED LINKS</span></span>
