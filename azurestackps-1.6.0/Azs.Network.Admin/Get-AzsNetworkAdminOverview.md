---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685238"
---
# <span data-ttu-id="ef7be-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="ef7be-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="ef7be-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef7be-102">SYNOPSIS</span></span>
<span data-ttu-id="ef7be-103">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="ef7be-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="ef7be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef7be-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="ef7be-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef7be-105">DESCRIPTION</span></span>
<span data-ttu-id="ef7be-106">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="ef7be-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="ef7be-107">Le singole proprietà includono un conteggio dettagliato dell'uso delle risorse e dell'integrità per componente.</span><span class="sxs-lookup"><span data-stu-id="ef7be-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="ef7be-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef7be-108">EXAMPLES</span></span>

### <span data-ttu-id="ef7be-109">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef7be-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="ef7be-110">Panoramica dell'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="ef7be-110">Get network admin overview.</span></span>

### <span data-ttu-id="ef7be-111">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef7be-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="ef7be-112">Ottenere l'utilizzo di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="ef7be-112">Get public ip address usage.</span></span>

## <span data-ttu-id="ef7be-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef7be-113">PARAMETERS</span></span>

### <span data-ttu-id="ef7be-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef7be-114">CommonParameters</span></span>
<span data-ttu-id="ef7be-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef7be-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef7be-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef7be-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef7be-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef7be-117">INPUTS</span></span>

## <span data-ttu-id="ef7be-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef7be-118">OUTPUTS</span></span>

### <span data-ttu-id="ef7be-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="ef7be-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="ef7be-120">Note</span><span class="sxs-lookup"><span data-stu-id="ef7be-120">NOTES</span></span>

## <span data-ttu-id="ef7be-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef7be-121">RELATED LINKS</span></span>

