---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360776"
---
# <span data-ttu-id="3ee4e-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="3ee4e-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="3ee4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ee4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee4e-103">Importa un oggetto JSON in una definizione di servizio Web.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="3ee4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ee4e-104">SYNTAX</span></span>

### <span data-ttu-id="3ee4e-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="3ee4e-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ee4e-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ee4e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ee4e-107">DESCRIPTION</span></span>
<span data-ttu-id="3ee4e-108">Il cmdlet Import-AzMlWebService importa, specificato direttamente o in un file a cui si fa riferimento, e crea un oggetto definizione di servizio Web che può essere passato al cmdlet New-AzMlWebService.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="3ee4e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ee4e-109">EXAMPLES</span></span>

### <span data-ttu-id="3ee4e-110">Esempio 1: importare da una stringa</span><span class="sxs-lookup"><span data-stu-id="3ee4e-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="3ee4e-111">Esempio 2: importare da un percorso di file</span><span class="sxs-lookup"><span data-stu-id="3ee4e-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="3ee4e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ee4e-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee4e-113">-DefaultProfile</span></span>
<span data-ttu-id="3ee4e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ee4e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ee4e-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3ee4e-115">-InputFile</span></span>
<span data-ttu-id="3ee4e-116">Percorso del file che contiene la definizione del servizio Web da importare.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee4e-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="3ee4e-117">-JsonString</span></span>
<span data-ttu-id="3ee4e-118">Stringa formattata JSON contenente la definizione del servizio Web da importare.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee4e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee4e-119">CommonParameters</span></span>
<span data-ttu-id="3ee4e-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee4e-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee4e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee4e-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ee4e-122">INPUTS</span></span>

### <span data-ttu-id="3ee4e-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3ee4e-123">None</span></span>

## <span data-ttu-id="3ee4e-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ee4e-124">OUTPUTS</span></span>

### <span data-ttu-id="3ee4e-125">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="3ee4e-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="3ee4e-126">Note</span><span class="sxs-lookup"><span data-stu-id="3ee4e-126">NOTES</span></span>
<span data-ttu-id="3ee4e-127">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="3ee4e-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3ee4e-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ee4e-128">RELATED LINKS</span></span>
