---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688084"
---
# <span data-ttu-id="e7694-101">Get-AzureRmExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="e7694-101">Get-AzureRmExpressRoutePortsLocation</span></span>

## <span data-ttu-id="e7694-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7694-102">SYNOPSIS</span></span>
<span data-ttu-id="e7694-103">Ottiene le posizioni in cui sono disponibili le risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e7694-103">Gets the locations at which ExpressRoutePort resources are available.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7694-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7694-104">SYNTAX</span></span>

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7694-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7694-105">DESCRIPTION</span></span>
<span data-ttu-id="e7694-106">Il cmdlet **Get-AzureRmExpressRoutePortsLocation** viene usato per recuperare le posizioni in cui sono disponibili le risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e7694-106">The **Get-AzureRmExpressRoutePortsLocation** cmdlet is used to retrieve the locations at which ExpressRoutePort resources are available.</span></span> <span data-ttu-id="e7694-107">Data una posizione specifica come input, il cmdlet Visualizza i dettagli di tale posizione, ovvero l'elenco delle larghezze di banda disponibili in tale posizione.</span><span class="sxs-lookup"><span data-stu-id="e7694-107">Given a specific location as input, the cmdlet displays the details of that location i.e., list of available bandwidths at that location.</span></span>


## <span data-ttu-id="e7694-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7694-108">EXAMPLES</span></span>

### <span data-ttu-id="e7694-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e7694-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

<span data-ttu-id="e7694-110">Elenca le posizioni in cui sono disponibili le risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="e7694-110">Lists the locations at which ExpressRoutePort resources are available.</span></span>

### <span data-ttu-id="e7694-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e7694-111">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

<span data-ttu-id="e7694-112">Elenca le larghezze di banda ExpressRoutePort disponibili in posizione $loc.</span><span class="sxs-lookup"><span data-stu-id="e7694-112">Lists the ExpressRoutePort bandwidths available at location $loc.</span></span>

## <span data-ttu-id="e7694-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7694-113">PARAMETERS</span></span>

### <span data-ttu-id="e7694-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7694-114">-DefaultProfile</span></span>
<span data-ttu-id="e7694-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7694-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7694-116">-LocationName</span><span class="sxs-lookup"><span data-stu-id="e7694-116">-LocationName</span></span>
<span data-ttu-id="e7694-117">Nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e7694-117">The name of the location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7694-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7694-118">CommonParameters</span></span>
<span data-ttu-id="e7694-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7694-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7694-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7694-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7694-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7694-121">INPUTS</span></span>

### <span data-ttu-id="e7694-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e7694-122">System.String</span></span>

## <span data-ttu-id="e7694-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7694-123">OUTPUTS</span></span>

### <span data-ttu-id="e7694-124">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePortsLocation</span><span class="sxs-lookup"><span data-stu-id="e7694-124">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation</span></span>

## <span data-ttu-id="e7694-125">Note</span><span class="sxs-lookup"><span data-stu-id="e7694-125">NOTES</span></span>

## <span data-ttu-id="e7694-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7694-126">RELATED LINKS</span></span>
