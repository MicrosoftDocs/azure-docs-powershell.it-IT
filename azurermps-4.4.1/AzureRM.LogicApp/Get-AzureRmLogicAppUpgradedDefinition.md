---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppUpgradedDefinition.md
ms.openlocfilehash: fda0c69f1df7df0939af3b788354111ddbaf8471
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688286"
---
# <span data-ttu-id="97aa4-101">Get-AzureRmLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="97aa4-101">Get-AzureRmLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="97aa4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="97aa4-103">Ottiene la definizione aggiornata per un'app logica.</span><span class="sxs-lookup"><span data-stu-id="97aa4-103">Gets the upgraded definition for a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97aa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97aa4-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97aa4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="97aa4-106">Il cmdlet **Get-AzureRmLogicAppUpgradedDefinition** ottiene la definizione aggiornata per la versione dello schema e l'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97aa4-106">The **Get-AzureRmLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="97aa4-107">Questo cmdlet restituisce un oggetto che rappresenta la definizione dell'app logica aggiornata.</span><span class="sxs-lookup"><span data-stu-id="97aa4-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="97aa4-108">Specificare il nome del gruppo di risorse, il nome dell'app logica e la versione dello schema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="97aa4-108">Specify the resource group name, logic app name, and target schema version.</span></span>

<span data-ttu-id="97aa4-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="97aa4-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="97aa4-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="97aa4-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="97aa4-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="97aa4-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="97aa4-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="97aa4-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="97aa4-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97aa4-113">EXAMPLES</span></span>

### <span data-ttu-id="97aa4-114">Esempio 1: ottenere una definizione aggiornata dell'app logica</span><span class="sxs-lookup"><span data-stu-id="97aa4-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzureRmLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="97aa4-115">Il primo comando consente di ottenere la definizione per l'app logica aggiornata alla versione dello schema di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="97aa4-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="97aa4-116">Il comando Archivia la definizione nella variabile $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="97aa4-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>

<span data-ttu-id="97aa4-117">Il secondo comando Visualizza il contenuto di $UpgradedDefinition come stringa.</span><span class="sxs-lookup"><span data-stu-id="97aa4-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="97aa4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97aa4-118">PARAMETERS</span></span>

### <span data-ttu-id="97aa4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="97aa4-119">-Name</span></span>
<span data-ttu-id="97aa4-120">Specifica il nome di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="97aa4-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97aa4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97aa4-121">-ResourceGroupName</span></span>
<span data-ttu-id="97aa4-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97aa4-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97aa4-123">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="97aa4-123">-TargetSchemaVersion</span></span>
<span data-ttu-id="97aa4-124">Specifica la versione dello schema di destinazione della definizione.</span><span class="sxs-lookup"><span data-stu-id="97aa4-124">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="97aa4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97aa4-125">-DefaultProfile</span></span>
<span data-ttu-id="97aa4-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97aa4-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97aa4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97aa4-127">CommonParameters</span></span>
<span data-ttu-id="97aa4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97aa4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97aa4-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97aa4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97aa4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97aa4-130">INPUTS</span></span>

## <span data-ttu-id="97aa4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97aa4-131">OUTPUTS</span></span>

### <span data-ttu-id="97aa4-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="97aa4-132">System.Object</span></span>

## <span data-ttu-id="97aa4-133">Note</span><span class="sxs-lookup"><span data-stu-id="97aa4-133">NOTES</span></span>

## <span data-ttu-id="97aa4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97aa4-134">RELATED LINKS</span></span>

[<span data-ttu-id="97aa4-135">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="97aa4-135">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)


