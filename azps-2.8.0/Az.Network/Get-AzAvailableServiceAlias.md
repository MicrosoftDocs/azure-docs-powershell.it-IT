---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: 7ea7bec01bacba43732f8e1eb544b109dfae11b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853273"
---
# <span data-ttu-id="53497-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="53497-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="53497-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53497-102">SYNOPSIS</span></span>
<span data-ttu-id="53497-103">Ottenere gli alias di servizio disponibili nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="53497-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="53497-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53497-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53497-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53497-105">DESCRIPTION</span></span>
<span data-ttu-id="53497-106">Il cmdlet **Get-AzAvailableServiceAlias** consente di recuperare tutti gli alias di servizio disponibili per una subnet nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="53497-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="53497-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53497-107">EXAMPLES</span></span>

### <span data-ttu-id="53497-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53497-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAliases -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="53497-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53497-109">PARAMETERS</span></span>

### <span data-ttu-id="53497-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53497-110">-DefaultProfile</span></span>
<span data-ttu-id="53497-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53497-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53497-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="53497-112">-Location</span></span>
<span data-ttu-id="53497-113">La posizione.</span><span class="sxs-lookup"><span data-stu-id="53497-113">The location.</span></span>

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

### <span data-ttu-id="53497-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53497-114">CommonParameters</span></span>
<span data-ttu-id="53497-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53497-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53497-116">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53497-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53497-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53497-117">INPUTS</span></span>

### <span data-ttu-id="53497-118">System. String</span><span class="sxs-lookup"><span data-stu-id="53497-118">System.String</span></span>

## <span data-ttu-id="53497-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53497-119">OUTPUTS</span></span>

### <span data-ttu-id="53497-120">Microsoft. Azure. Commands. Network. Models. PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="53497-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="53497-121">Note</span><span class="sxs-lookup"><span data-stu-id="53497-121">NOTES</span></span>

## <span data-ttu-id="53497-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53497-122">RELATED LINKS</span></span>
