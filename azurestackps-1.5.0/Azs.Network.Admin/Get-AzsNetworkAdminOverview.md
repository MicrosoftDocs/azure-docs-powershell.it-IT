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
ms.locfileid: "93491114"
---
# <span data-ttu-id="6a44f-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="6a44f-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="6a44f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a44f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a44f-103">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="6a44f-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="6a44f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a44f-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="6a44f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a44f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a44f-106">Ottenere una panoramica dello stato del provider di risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="6a44f-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="6a44f-107">Le singole proprietà includono un conteggio dettagliato dell'uso delle risorse e dell'integrità per componente.</span><span class="sxs-lookup"><span data-stu-id="6a44f-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="6a44f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a44f-108">EXAMPLES</span></span>

### <span data-ttu-id="6a44f-109">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a44f-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="6a44f-110">Panoramica dell'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="6a44f-110">Get network admin overview.</span></span>

### <span data-ttu-id="6a44f-111">--------------------------ESEMPIO 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="6a44f-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="6a44f-112">Ottenere l'utilizzo di indirizzi IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="6a44f-112">Get public ip address usage.</span></span>

## <span data-ttu-id="6a44f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a44f-113">PARAMETERS</span></span>

### <span data-ttu-id="6a44f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a44f-114">CommonParameters</span></span>
<span data-ttu-id="6a44f-115">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a44f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a44f-116">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a44f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a44f-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a44f-117">INPUTS</span></span>

## <span data-ttu-id="6a44f-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a44f-118">OUTPUTS</span></span>

### <span data-ttu-id="6a44f-119">Microsoft. AzureStack. Management. Network. admin. Models. AdminOverview</span><span class="sxs-lookup"><span data-stu-id="6a44f-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="6a44f-120">Note</span><span class="sxs-lookup"><span data-stu-id="6a44f-120">NOTES</span></span>

## <span data-ttu-id="6a44f-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a44f-121">RELATED LINKS</span></span>

