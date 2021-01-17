---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386063"
---
# <span data-ttu-id="ab002-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ab002-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="ab002-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab002-102">SYNOPSIS</span></span>
<span data-ttu-id="ab002-103">Esporta l'oggetto definizione di servizio Web come stringa formattata JSON.</span><span class="sxs-lookup"><span data-stu-id="ab002-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="ab002-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab002-104">SYNTAX</span></span>

### <span data-ttu-id="ab002-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="ab002-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab002-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="ab002-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab002-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab002-107">DESCRIPTION</span></span>
<span data-ttu-id="ab002-108">Esporta l'oggetto Definition per il servizio Web specificato come stringa formattata JSON.</span><span class="sxs-lookup"><span data-stu-id="ab002-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="ab002-109">Puoi restituire immediatamente la stringa o salvarla in un file.</span><span class="sxs-lookup"><span data-stu-id="ab002-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="ab002-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab002-110">EXAMPLES</span></span>

### <span data-ttu-id="ab002-111">Esempio 1: esportare come stringa</span><span class="sxs-lookup"><span data-stu-id="ab002-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="ab002-112">Esempio 2: esportare in un file</span><span class="sxs-lookup"><span data-stu-id="ab002-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="ab002-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab002-113">PARAMETERS</span></span>

### <span data-ttu-id="ab002-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab002-114">-DefaultProfile</span></span>
<span data-ttu-id="ab002-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab002-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab002-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ab002-116">-Force</span></span>
<span data-ttu-id="ab002-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ab002-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ab002-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ab002-118">-OutputFile</span></span>
<span data-ttu-id="ab002-119">Percorso del file per la definizione esportata.</span><span class="sxs-lookup"><span data-stu-id="ab002-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="ab002-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="ab002-120">-ToJsonString</span></span>
<span data-ttu-id="ab002-121">Specifica che la definizione verrà esportata come stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="ab002-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="ab002-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="ab002-122">-WebService</span></span>
<span data-ttu-id="ab002-123">Oggetto definizione del servizio Web da esportare.</span><span class="sxs-lookup"><span data-stu-id="ab002-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="ab002-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab002-124">-Confirm</span></span>
<span data-ttu-id="ab002-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab002-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab002-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab002-126">-WhatIf</span></span>
<span data-ttu-id="ab002-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab002-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab002-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab002-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab002-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab002-129">CommonParameters</span></span>
<span data-ttu-id="ab002-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab002-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab002-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab002-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab002-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab002-132">INPUTS</span></span>

### <span data-ttu-id="ab002-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="ab002-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ab002-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab002-134">OUTPUTS</span></span>

### <span data-ttu-id="ab002-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ab002-135">System.String</span></span>

## <span data-ttu-id="ab002-136">Note</span><span class="sxs-lookup"><span data-stu-id="ab002-136">NOTES</span></span>
<span data-ttu-id="ab002-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ab002-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ab002-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab002-138">RELATED LINKS</span></span>
