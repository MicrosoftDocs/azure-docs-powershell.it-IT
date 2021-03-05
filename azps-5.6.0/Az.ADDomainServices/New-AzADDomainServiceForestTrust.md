---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceForestTrust
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceForestTrust.md
ms.openlocfilehash: aaf3fa74000bd5ab7264386b28fe20588235c951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986312"
---
# <span data-ttu-id="176a2-101">New-AzADDomainServiceForestTrust</span><span class="sxs-lookup"><span data-stu-id="176a2-101">New-AzADDomainServiceForestTrust</span></span>

## <span data-ttu-id="176a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176a2-102">SYNOPSIS</span></span>
<span data-ttu-id="176a2-103">Creare un oggetto in memoria per ForestTrust</span><span class="sxs-lookup"><span data-stu-id="176a2-103">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="176a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="176a2-104">SYNTAX</span></span>

```
New-AzADDomainServiceForestTrust [-FriendlyName <String>] [-RemoteDnsIP <String>] [-TrustDirection <String>]
 [-TrustedDomainFqdn <String>] [-TrustPassword <SecureString>] [<CommonParameters>]
```

## <span data-ttu-id="176a2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="176a2-105">DESCRIPTION</span></span>
<span data-ttu-id="176a2-106">Creare un oggetto in memoria per ForestTrust</span><span class="sxs-lookup"><span data-stu-id="176a2-106">Create a in-memory object for ForestTrust</span></span>

## <span data-ttu-id="176a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="176a2-107">EXAMPLES</span></span>

### <span data-ttu-id="176a2-108">Esempio 1: Creare ServiceForestTrust per ADDomain</span><span class="sxs-lookup"><span data-stu-id="176a2-108">Example 1: Create ServiceForestTrust for ADDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceForestTrust -FriendlyName FriendlyNameTest

FriendlyName     RemoteDnsIP TrustDirection TrustPassword TrustedDomainFqdn
------------     ----------- -------------- ------------- -----------------
FriendlyNameTest
```

<span data-ttu-id="176a2-109">Creare ServiceForestTrust per ADDomain</span><span class="sxs-lookup"><span data-stu-id="176a2-109">Create ServiceForestTrust for ADDomain</span></span>

## <span data-ttu-id="176a2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176a2-110">PARAMETERS</span></span>

### <span data-ttu-id="176a2-111">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="176a2-111">-FriendlyName</span></span>
<span data-ttu-id="176a2-112">Nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="176a2-112">Friendly Name.</span></span>

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

### <span data-ttu-id="176a2-113">-RemoteDnsIP</span><span class="sxs-lookup"><span data-stu-id="176a2-113">-RemoteDnsIP</span></span>
<span data-ttu-id="176a2-114">Ip Dns remoti.</span><span class="sxs-lookup"><span data-stu-id="176a2-114">Remote Dns ips.</span></span>

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

### <span data-ttu-id="176a2-115">-TrustDirection</span><span class="sxs-lookup"><span data-stu-id="176a2-115">-TrustDirection</span></span>
<span data-ttu-id="176a2-116">Direzione protezione.</span><span class="sxs-lookup"><span data-stu-id="176a2-116">Trust Direction.</span></span>

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

### <span data-ttu-id="176a2-117">-TrustedDomainFqdn</span><span class="sxs-lookup"><span data-stu-id="176a2-117">-TrustedDomainFqdn</span></span>
<span data-ttu-id="176a2-118">FQDN dominio attendibile.</span><span class="sxs-lookup"><span data-stu-id="176a2-118">Trusted Domain FQDN.</span></span>

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

### <span data-ttu-id="176a2-119">-TrustPassword</span><span class="sxs-lookup"><span data-stu-id="176a2-119">-TrustPassword</span></span>
<span data-ttu-id="176a2-120">Password di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="176a2-120">Trust Password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="176a2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176a2-121">CommonParameters</span></span>
<span data-ttu-id="176a2-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176a2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176a2-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="176a2-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176a2-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="176a2-124">INPUTS</span></span>

## <span data-ttu-id="176a2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="176a2-125">OUTPUTS</span></span>

### <span data-ttu-id="176a2-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span><span class="sxs-lookup"><span data-stu-id="176a2-126">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ForestTrust</span></span>

## <span data-ttu-id="176a2-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="176a2-127">NOTES</span></span>

<span data-ttu-id="176a2-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="176a2-128">ALIASES</span></span>

## <span data-ttu-id="176a2-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="176a2-129">RELATED LINKS</span></span>

