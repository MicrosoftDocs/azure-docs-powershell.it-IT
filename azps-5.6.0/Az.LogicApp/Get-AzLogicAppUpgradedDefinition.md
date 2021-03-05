---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 1be662b88b487fbf79092c30f8bd7277adc9e3cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008877"
---
# <span data-ttu-id="594c0-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="594c0-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="594c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="594c0-102">SYNOPSIS</span></span>
<span data-ttu-id="594c0-103">Ottiene la definizione aggiornata per un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="594c0-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="594c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="594c0-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="594c0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="594c0-105">DESCRIPTION</span></span>
<span data-ttu-id="594c0-106">Il cmdlet **Get-AzLogicAppUpgradedDefinition** ottiene la definizione aggiornata per l'app per la versione e la logica dello schema da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="594c0-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="594c0-107">Questo cmdlet restituisce un oggetto che rappresenta la definizione dell'app per la logica aggiornata.</span><span class="sxs-lookup"><span data-stu-id="594c0-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="594c0-108">Specificare il nome del gruppo di risorse, il nome dell'app per la logica e la versione dello schema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="594c0-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="594c0-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="594c0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="594c0-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="594c0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="594c0-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="594c0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="594c0-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="594c0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="594c0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="594c0-113">EXAMPLES</span></span>

### <span data-ttu-id="594c0-114">Esempio 1: Ottenere una definizione aggiornata di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="594c0-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
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

<span data-ttu-id="594c0-115">Il primo comando ottiene la definizione per l'app logica aggiornata alla versione dello schema di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="594c0-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="594c0-116">Il comando archivia la definizione nella $UpgradedDefinition variabile.</span><span class="sxs-lookup"><span data-stu-id="594c0-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="594c0-117">Il secondo comando visualizza il contenuto della $UpgradedDefinition come stringa.</span><span class="sxs-lookup"><span data-stu-id="594c0-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="594c0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="594c0-118">PARAMETERS</span></span>

### <span data-ttu-id="594c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594c0-119">-DefaultProfile</span></span>
<span data-ttu-id="594c0-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="594c0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="594c0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="594c0-121">-Name</span></span>
<span data-ttu-id="594c0-122">Specifica il nome di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="594c0-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="594c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="594c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="594c0-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="594c0-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="594c0-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="594c0-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="594c0-126">Specifica la versione dello schema di destinazione della definizione.</span><span class="sxs-lookup"><span data-stu-id="594c0-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="594c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594c0-127">CommonParameters</span></span>
<span data-ttu-id="594c0-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="594c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594c0-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="594c0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594c0-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="594c0-130">INPUTS</span></span>

### <span data-ttu-id="594c0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="594c0-131">System.String</span></span>

## <span data-ttu-id="594c0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="594c0-132">OUTPUTS</span></span>

### <span data-ttu-id="594c0-133">System.Object</span><span class="sxs-lookup"><span data-stu-id="594c0-133">System.Object</span></span>

## <span data-ttu-id="594c0-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="594c0-134">NOTES</span></span>

## <span data-ttu-id="594c0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="594c0-135">RELATED LINKS</span></span>

[<span data-ttu-id="594c0-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="594c0-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


