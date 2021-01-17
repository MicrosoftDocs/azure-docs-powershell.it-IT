---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474104"
---
# <span data-ttu-id="1c28d-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="1c28d-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="1c28d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c28d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c28d-103">Ottiene la definizione aggiornata per un'app logica.</span><span class="sxs-lookup"><span data-stu-id="1c28d-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="1c28d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c28d-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c28d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c28d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c28d-106">Il cmdlet **Get-AzLogicAppUpgradedDefinition** ottiene la definizione aggiornata per la versione dello schema e l'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c28d-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="1c28d-107">Questo cmdlet restituisce un oggetto che rappresenta la definizione dell'app logica aggiornata.</span><span class="sxs-lookup"><span data-stu-id="1c28d-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="1c28d-108">Specificare il nome del gruppo di risorse, il nome dell'app logica e la versione dello schema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1c28d-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="1c28d-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="1c28d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1c28d-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="1c28d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1c28d-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="1c28d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1c28d-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="1c28d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1c28d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c28d-113">EXAMPLES</span></span>

### <span data-ttu-id="1c28d-114">Esempio 1: ottenere una definizione aggiornata dell'app logica</span><span class="sxs-lookup"><span data-stu-id="1c28d-114">Example 1: Get a logic app upgraded definition</span></span>
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

<span data-ttu-id="1c28d-115">Il primo comando consente di ottenere la definizione per l'app logica aggiornata alla versione dello schema di destinazione specificata.</span><span class="sxs-lookup"><span data-stu-id="1c28d-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="1c28d-116">Il comando Archivia la definizione nella variabile $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="1c28d-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="1c28d-117">Il secondo comando Visualizza il contenuto di $UpgradedDefinition come stringa.</span><span class="sxs-lookup"><span data-stu-id="1c28d-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="1c28d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c28d-118">PARAMETERS</span></span>

### <span data-ttu-id="1c28d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c28d-119">-DefaultProfile</span></span>
<span data-ttu-id="1c28d-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1c28d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c28d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c28d-121">-Name</span></span>
<span data-ttu-id="1c28d-122">Specifica il nome di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="1c28d-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="1c28d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c28d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1c28d-124">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c28d-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c28d-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="1c28d-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="1c28d-126">Specifica la versione dello schema di destinazione della definizione.</span><span class="sxs-lookup"><span data-stu-id="1c28d-126">Specifies the target schema version of the definition.</span></span>

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

### <span data-ttu-id="1c28d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c28d-127">CommonParameters</span></span>
<span data-ttu-id="1c28d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c28d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c28d-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c28d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c28d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c28d-130">INPUTS</span></span>

### <span data-ttu-id="1c28d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1c28d-131">System.String</span></span>

## <span data-ttu-id="1c28d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c28d-132">OUTPUTS</span></span>

### <span data-ttu-id="1c28d-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="1c28d-133">System.Object</span></span>

## <span data-ttu-id="1c28d-134">Note</span><span class="sxs-lookup"><span data-stu-id="1c28d-134">NOTES</span></span>

## <span data-ttu-id="1c28d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c28d-135">RELATED LINKS</span></span>

[<span data-ttu-id="1c28d-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1c28d-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


