---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoormanagedruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorManagedRuleObject.md
ms.openlocfilehash: 236cb9ff263f97ae52ea5d3226f4defec00c662a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686392"
---
# <span data-ttu-id="b7090-101">New-AzureRmFrontDoorManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="b7090-101">New-AzureRmFrontDoorManagedRuleObject</span></span>

## <span data-ttu-id="b7090-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7090-102">SYNOPSIS</span></span>
<span data-ttu-id="b7090-103">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="b7090-103">Create ManagedRule Object for WAF policy creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7090-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7090-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorManagedRuleObject -Priority <Int32> [-Version <String>]
 [-RuleGroupOverride <PSAzureRuleGroupOverride[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7090-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7090-105">DESCRIPTION</span></span>
<span data-ttu-id="b7090-106">Creare un oggetto ManagedRule per la creazione di criteri WAF</span><span class="sxs-lookup"><span data-stu-id="b7090-106">Create ManagedRule Object for WAF policy creation</span></span>

## <span data-ttu-id="b7090-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7090-107">EXAMPLES</span></span>

### <span data-ttu-id="b7090-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7090-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor
ManagedRuleObject -Priority 1 -Version 0 -RuleGroupOverride $override1

RuleGroupOverrides                                                   Priority Version
------------------                                                   -------- -------
{Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride}        1 0
```

<span data-ttu-id="b7090-109">Creare un oggetto ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b7090-109">Create a ManagedRule Object</span></span>

## <span data-ttu-id="b7090-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7090-110">PARAMETERS</span></span>

### <span data-ttu-id="b7090-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7090-111">-DefaultProfile</span></span>
<span data-ttu-id="b7090-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7090-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7090-113">-Priorità</span><span class="sxs-lookup"><span data-stu-id="b7090-113">-Priority</span></span>
<span data-ttu-id="b7090-114">Descrive la priorità della regola</span><span class="sxs-lookup"><span data-stu-id="b7090-114">Describes priority of the rule</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7090-115">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="b7090-115">-RuleGroupOverride</span></span>
<span data-ttu-id="b7090-116">Elenco della configurazione di override di Azure Managed provider</span><span class="sxs-lookup"><span data-stu-id="b7090-116">List of azure managed provider override configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSAzureRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7090-117">-Versione</span><span class="sxs-lookup"><span data-stu-id="b7090-117">-Version</span></span>
<span data-ttu-id="b7090-118">Versione del set di regole</span><span class="sxs-lookup"><span data-stu-id="b7090-118">Version of the ruleset</span></span>

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

### <span data-ttu-id="b7090-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7090-119">CommonParameters</span></span>
<span data-ttu-id="b7090-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7090-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7090-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7090-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7090-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7090-122">INPUTS</span></span>

### <span data-ttu-id="b7090-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7090-123">None</span></span>

## <span data-ttu-id="b7090-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7090-124">OUTPUTS</span></span>

### <span data-ttu-id="b7090-125">Microsoft. Azure. Commands. FrontDoor. Models. PSAzureManagedRule</span><span class="sxs-lookup"><span data-stu-id="b7090-125">Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule</span></span>

## <span data-ttu-id="b7090-126">Note</span><span class="sxs-lookup"><span data-stu-id="b7090-126">NOTES</span></span>

## <span data-ttu-id="b7090-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7090-127">RELATED LINKS</span></span>

<span data-ttu-id="b7090-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span><span class="sxs-lookup"><span data-stu-id="b7090-128">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorRuleGroupOverrideObject](./Set-AzureRmFrontDoorRuleGroupOverrideObject.md)</span></span>
