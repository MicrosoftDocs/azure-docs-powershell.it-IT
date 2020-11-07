---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslpredefinedpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 7a0ab0643b00de314d1e969e1d38bcc7ff4b4d86
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865037"
---
# <span data-ttu-id="6285c-101">Get-AzApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="6285c-101">Get-AzApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="6285c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6285c-102">SYNOPSIS</span></span>
<span data-ttu-id="6285c-103">Ottiene i criteri SSL predefiniti forniti dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6285c-103">Gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="6285c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6285c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6285c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6285c-105">DESCRIPTION</span></span>
<span data-ttu-id="6285c-106">Il cmdlet **Get-AzApplicationGatewaySslPredefinedPolicy** ottiene i criteri SSL predefiniti forniti dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6285c-106">The **Get-AzApplicationGatewaySslPredefinedPolicy** cmdlet gets Predefined SSL Policies provided by Application Gateway.</span></span>

## <span data-ttu-id="6285c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6285c-107">EXAMPLES</span></span>

### <span data-ttu-id="6285c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6285c-108">Example 1</span></span>
```
PS C:\> Get-AzApplicationGatewaySslPredefinedPolicy

Name: AppGwSslPolicy20150501
MinProtocolVersion: TLSv1_0
CipherSuites:
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_DHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_DHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_DHE_RSA_WITH_AES_256_CBC_SHA
    TLS_DHE_RSA_WITH_AES_128_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_DHE_DSS_WITH_AES_256_CBC_SHA256
    TLS_DHE_DSS_WITH_AES_128_CBC_SHA256
    TLS_DHE_DSS_WITH_AES_256_CBC_SHA
    TLS_DHE_DSS_WITH_AES_128_CBC_SHA
    TLS_RSA_WITH_3DES_EDE_CBC_SHA
    TLS_DHE_DSS_WITH_3DES_EDE_CBC_SHA


Name: AppGwSslPolicy20170401
MinProtocolVersion: TLSv1_1
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA


Name: AppGwSslPolicy20170401S
MinProtocolVersion: TLSv1_2
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
```

<span data-ttu-id="6285c-109">Questi comandi restituiscono tutti i criteri SSL predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6285c-109">This commands returns all the predefined SSL policies.</span></span>

### <span data-ttu-id="6285c-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6285c-110">Example 2</span></span>
```
PS C:\> Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401

Name: AppGwSslPolicy20170401
MinProtocolVersion: TLSv1_1
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
```

<span data-ttu-id="6285c-111">Questo comando restituisce un criterio predefinito con il nome AppGwSslPolicy20170401.</span><span class="sxs-lookup"><span data-stu-id="6285c-111">This commands returns predefined policy with name AppGwSslPolicy20170401.</span></span>

### <span data-ttu-id="6285c-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6285c-112">Example 3</span></span>
```
PS C:\> Get-AzApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy2017*

Name: AppGwSslPolicy20170401
MinProtocolVersion: TLSv1_1
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA


Name: AppGwSslPolicy20170401S
MinProtocolVersion: TLSv1_2
CipherSuites:
    TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA
    TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256
    TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384
    TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384
    TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
    TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA
    TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_256_GCM_SHA384
    TLS_RSA_WITH_AES_128_GCM_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA256
    TLS_RSA_WITH_AES_128_CBC_SHA256
    TLS_RSA_WITH_AES_256_CBC_SHA
    TLS_RSA_WITH_AES_128_CBC_SHA
```

<span data-ttu-id="6285c-113">Questo comando restituisce un criterio predefinito con il nome che inizia con "AppGwSslPolicy2017".</span><span class="sxs-lookup"><span data-stu-id="6285c-113">This commands returns predefined policy with name starting with "AppGwSslPolicy2017".</span></span>

## <span data-ttu-id="6285c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6285c-114">PARAMETERS</span></span>

### <span data-ttu-id="6285c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6285c-115">-DefaultProfile</span></span>
<span data-ttu-id="6285c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6285c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6285c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6285c-117">-Name</span></span>
<span data-ttu-id="6285c-118">Nome del criterio predefinito SSL</span><span class="sxs-lookup"><span data-stu-id="6285c-118">Name of the ssl predefined policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6285c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6285c-119">CommonParameters</span></span>
<span data-ttu-id="6285c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6285c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6285c-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6285c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6285c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6285c-122">INPUTS</span></span>

### <span data-ttu-id="6285c-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6285c-123">None</span></span>

## <span data-ttu-id="6285c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6285c-124">OUTPUTS</span></span>

### <span data-ttu-id="6285c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPredefinedPolicy</span><span class="sxs-lookup"><span data-stu-id="6285c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPredefinedPolicy</span></span>

## <span data-ttu-id="6285c-126">Note</span><span class="sxs-lookup"><span data-stu-id="6285c-126">NOTES</span></span>

## <span data-ttu-id="6285c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6285c-127">RELATED LINKS</span></span>
