---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 6e8c3cdbfa1242cba19d3aa3250c4bf4e381ae92
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347452"
---
# <span data-ttu-id="a4e4f-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4e4f-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="a4e4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e4f-103">Crea una nuova configurazione di autenticazione client per il profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="a4e4f-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="a4e4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4e4f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4e4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4e4f-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e4f-106">Il cmdlet **New-AzApplicationGatewayClientAuthConfiguration** crea una nuova configurazione di autenticazione client per il profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="a4e4f-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="a4e4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4e4f-107">EXAMPLES</span></span>

### <span data-ttu-id="a4e4f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4e4f-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="a4e4f-109">Il comando crea una nuova configurazione di autenticazione client e la archivia in $clientAuthConfig variabile da usare in un profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="a4e4f-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="a4e4f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4e4f-110">PARAMETERS</span></span>

### <span data-ttu-id="a4e4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e4f-111">-DefaultProfile</span></span>
<span data-ttu-id="a4e4f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e4f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e4f-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="a4e4f-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="a4e4f-114">Verificare il nome dell'autorità di certificazione del certificato client.</span><span class="sxs-lookup"><span data-stu-id="a4e4f-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4e4f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e4f-115">CommonParameters</span></span>
<span data-ttu-id="a4e4f-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4e4f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e4f-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4e4f-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e4f-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4e4f-118">INPUTS</span></span>

### <span data-ttu-id="a4e4f-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a4e4f-119">None</span></span>

## <span data-ttu-id="a4e4f-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4e4f-120">OUTPUTS</span></span>

### <span data-ttu-id="a4e4f-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4e4f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="a4e4f-122">Note</span><span class="sxs-lookup"><span data-stu-id="a4e4f-122">NOTES</span></span>

## <span data-ttu-id="a4e4f-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4e4f-123">RELATED LINKS</span></span>

[<span data-ttu-id="a4e4f-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4e4f-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a4e4f-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4e4f-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a4e4f-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4e4f-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="a4e4f-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="a4e4f-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)