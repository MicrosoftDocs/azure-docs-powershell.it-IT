---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f5fbef7c67676f16793b63a8448517ca24aa7e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030077"
---
# <span data-ttu-id="6756f-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="6756f-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="6756f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6756f-102">SYNOPSIS</span></span>
<span data-ttu-id="6756f-103">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="6756f-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="6756f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6756f-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="6756f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6756f-105">DESCRIPTION</span></span>
<span data-ttu-id="6756f-106">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="6756f-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="6756f-107">Le singole proprietà includono un conteggio dettagliato dell'uso delle risorse e dell'integrità per componente.</span><span class="sxs-lookup"><span data-stu-id="6756f-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="6756f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6756f-108">EXAMPLES</span></span>

### <span data-ttu-id="6756f-109">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="6756f-109">EXAMPLE 1</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="6756f-110">Panoramica dell'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="6756f-110">Get network admin overview.</span></span>

### <span data-ttu-id="6756f-111">ESEMPIO 2</span><span class="sxs-lookup"><span data-stu-id="6756f-111">EXAMPLE 2</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="6756f-112">Ottenere l'utilizzo di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="6756f-112">Get public ip address usage.</span></span>

## <span data-ttu-id="6756f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6756f-113">PARAMETERS</span></span>

### <span data-ttu-id="6756f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6756f-114">CommonParameters</span></span>
<span data-ttu-id="6756f-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6756f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6756f-116">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6756f-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6756f-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6756f-117">INPUTS</span></span>

## <span data-ttu-id="6756f-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6756f-118">OUTPUTS</span></span>

### <span data-ttu-id="6756f-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="6756f-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="6756f-120">Note</span><span class="sxs-lookup"><span data-stu-id="6756f-120">NOTES</span></span>

## <span data-ttu-id="6756f-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6756f-121">RELATED LINKS</span></span>
