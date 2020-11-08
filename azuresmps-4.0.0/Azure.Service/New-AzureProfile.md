---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023958"
---
# <span data-ttu-id="5a6ca-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="5a6ca-101">New-AzureProfile</span></span>

## <span data-ttu-id="5a6ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a6ca-102">SYNOPSIS</span></span>

## <span data-ttu-id="5a6ca-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a6ca-103">SYNTAX</span></span>

### <span data-ttu-id="5a6ca-104">Certificato</span><span class="sxs-lookup"><span data-stu-id="5a6ca-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="5a6ca-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a6ca-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="5a6ca-106">Token</span><span class="sxs-lookup"><span data-stu-id="5a6ca-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="5a6ca-107">Credenziali</span><span class="sxs-lookup"><span data-stu-id="5a6ca-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="5a6ca-108">Vuoto</span><span class="sxs-lookup"><span data-stu-id="5a6ca-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="5a6ca-109">File</span><span class="sxs-lookup"><span data-stu-id="5a6ca-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="5a6ca-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="5a6ca-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="5a6ca-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a6ca-111">DESCRIPTION</span></span>

## <span data-ttu-id="5a6ca-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a6ca-112">EXAMPLES</span></span>

### <span data-ttu-id="5a6ca-113">1:</span><span class="sxs-lookup"><span data-stu-id="5a6ca-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="5a6ca-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a6ca-114">PARAMETERS</span></span>

### <span data-ttu-id="5a6ca-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="5a6ca-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="5a6ca-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-117">-Certificato</span><span class="sxs-lookup"><span data-stu-id="5a6ca-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-118">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="5a6ca-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-119">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="5a6ca-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-120">-Path</span><span class="sxs-lookup"><span data-stu-id="5a6ca-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-121">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="5a6ca-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5a6ca-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5a6ca-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a6ca-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-125">-Tenant</span><span class="sxs-lookup"><span data-stu-id="5a6ca-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6ca-126">CommonParameters</span></span>
<span data-ttu-id="5a6ca-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6ca-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a6ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6ca-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a6ca-129">INPUTS</span></span>

## <span data-ttu-id="5a6ca-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a6ca-130">OUTPUTS</span></span>

## <span data-ttu-id="5a6ca-131">Note</span><span class="sxs-lookup"><span data-stu-id="5a6ca-131">NOTES</span></span>

## <span data-ttu-id="5a6ca-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a6ca-132">RELATED LINKS</span></span>

