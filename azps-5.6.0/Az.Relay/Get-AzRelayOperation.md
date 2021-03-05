---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 72f9e3290af5aad665213c1ffdebf5f3b2edcf92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000605"
---
# <span data-ttu-id="377f5-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="377f5-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="377f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="377f5-102">SYNOPSIS</span></span>
<span data-ttu-id="377f5-103">Elencare le operazioni di inoltro supportate</span><span class="sxs-lookup"><span data-stu-id="377f5-103">List supported Relay Operations</span></span>

## <span data-ttu-id="377f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="377f5-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="377f5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="377f5-105">DESCRIPTION</span></span>
<span data-ttu-id="377f5-106">Il **cmdlet Get-AzRelayOperation** elenca le operazioni supportate dall'inoltro.</span><span class="sxs-lookup"><span data-stu-id="377f5-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="377f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="377f5-107">EXAMPLES</span></span>

### <span data-ttu-id="377f5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="377f5-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="377f5-109">Elenca le operazioni supportate da Inoltro</span><span class="sxs-lookup"><span data-stu-id="377f5-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="377f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="377f5-110">PARAMETERS</span></span>

### <span data-ttu-id="377f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377f5-111">-DefaultProfile</span></span>
<span data-ttu-id="377f5-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="377f5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377f5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377f5-113">CommonParameters</span></span>
<span data-ttu-id="377f5-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="377f5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377f5-115">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="377f5-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377f5-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="377f5-116">INPUTS</span></span>

### <span data-ttu-id="377f5-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="377f5-117">None</span></span>

## <span data-ttu-id="377f5-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="377f5-118">OUTPUTS</span></span>

### <span data-ttu-id="377f5-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="377f5-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="377f5-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="377f5-120">NOTES</span></span>

## <span data-ttu-id="377f5-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="377f5-121">RELATED LINKS</span></span>
