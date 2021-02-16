---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableservicealias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailableServiceAlias.md
ms.openlocfilehash: acf9d604a793d4631641a87b222260d8687807cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193895"
---
# <span data-ttu-id="74f7a-101">Get-AzAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="74f7a-101">Get-AzAvailableServiceAlias</span></span>

## <span data-ttu-id="74f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="74f7a-103">Ottenere gli alias di servizio disponibili nell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="74f7a-103">Get available service aliases in the region.</span></span>

## <span data-ttu-id="74f7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74f7a-104">SYNTAX</span></span>

```
Get-AzAvailableServiceAlias -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74f7a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="74f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="74f7a-106">Il cmdlet **Get-AzAvailableServiceAlias** consente di recuperare tutti gli alias di servizio disponibili per una subnet nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="74f7a-106">The **Get-AzAvailableServiceAlias** cmdlet allows you to retrieve all of the available service aliases for a subnet in the provided location.</span></span>

## <span data-ttu-id="74f7a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74f7a-107">EXAMPLES</span></span>

### <span data-ttu-id="74f7a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74f7a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAvailableServiceAlias -Location "westus"

Name                         Id                                                                                                                                   Type                                      ResourceName
----                         --                                                                                                                                   ----                                      ------------
servicesAzure                /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzure                Microsoft.Network/AvailableServiceAliases /services/Azure
servicesAzureManagedInstance /subscriptions/61dc4623-b5f8-41a0-acfc-29537dcf6e5d/providers/Microsoft.Network/AvailableServiceAliases/servicesAzureManagedInstance Microsoft.Network/AvailableServiceAliases /services/Azure/ManagedInstance

```

## <span data-ttu-id="74f7a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74f7a-109">PARAMETERS</span></span>

### <span data-ttu-id="74f7a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f7a-110">-DefaultProfile</span></span>
<span data-ttu-id="74f7a-111">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74f7a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74f7a-112">-Location</span><span class="sxs-lookup"><span data-stu-id="74f7a-112">-Location</span></span>
<span data-ttu-id="74f7a-113">Posizione.</span><span class="sxs-lookup"><span data-stu-id="74f7a-113">The location.</span></span>

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

### <span data-ttu-id="74f7a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f7a-114">CommonParameters</span></span>
<span data-ttu-id="74f7a-115">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f7a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f7a-116">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74f7a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f7a-117">INPUT</span><span class="sxs-lookup"><span data-stu-id="74f7a-117">INPUTS</span></span>

### <span data-ttu-id="74f7a-118">System.String</span><span class="sxs-lookup"><span data-stu-id="74f7a-118">System.String</span></span>

## <span data-ttu-id="74f7a-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74f7a-119">OUTPUTS</span></span>

### <span data-ttu-id="74f7a-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span><span class="sxs-lookup"><span data-stu-id="74f7a-120">Microsoft.Azure.Commands.Network.Models.PsAvailableServiceAlias</span></span>

## <span data-ttu-id="74f7a-121">NOTE</span><span class="sxs-lookup"><span data-stu-id="74f7a-121">NOTES</span></span>

## <span data-ttu-id="74f7a-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74f7a-122">RELATED LINKS</span></span>
