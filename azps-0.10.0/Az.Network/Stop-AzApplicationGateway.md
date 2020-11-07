---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 97dc4b46f4a9156bc43e7902d50414a586d0f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862685"
---
# <span data-ttu-id="800d1-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="800d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="800d1-102">SYNOPSIS</span></span>
<span data-ttu-id="800d1-103">Interrompe un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="800d1-103">Stops an application gateway</span></span>

## <span data-ttu-id="800d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="800d1-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="800d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="800d1-105">DESCRIPTION</span></span>
<span data-ttu-id="800d1-106">Il cmdlet **Stop-AzApplicationGateway** arresta un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="800d1-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="800d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="800d1-107">EXAMPLES</span></span>

### <span data-ttu-id="800d1-108">Esempio 1: arrestare un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="800d1-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="800d1-109">Questo comando Arresta il gateway dell'applicazione archiviato nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="800d1-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="800d1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="800d1-110">PARAMETERS</span></span>

### <span data-ttu-id="800d1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-111">-ApplicationGateway</span></span>
<span data-ttu-id="800d1-112">Specifica il gateway dell'applicazione che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="800d1-112">Specifies the application gateway that this cmdlet stops.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="800d1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="800d1-113">-AsJob</span></span>
<span data-ttu-id="800d1-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="800d1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="800d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800d1-115">-DefaultProfile</span></span>
<span data-ttu-id="800d1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="800d1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800d1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800d1-117">CommonParameters</span></span>
<span data-ttu-id="800d1-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800d1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800d1-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="800d1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800d1-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="800d1-120">INPUTS</span></span>

### <span data-ttu-id="800d1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="800d1-121">System.String</span></span>

## <span data-ttu-id="800d1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="800d1-122">OUTPUTS</span></span>

### <span data-ttu-id="800d1-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="800d1-124">Note</span><span class="sxs-lookup"><span data-stu-id="800d1-124">NOTES</span></span>

## <span data-ttu-id="800d1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="800d1-125">RELATED LINKS</span></span>

[<span data-ttu-id="800d1-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="800d1-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="800d1-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="800d1-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="800d1-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="800d1-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


