---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192753"
---
# <span data-ttu-id="b580a-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b580a-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="b580a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b580a-102">SYNOPSIS</span></span>
<span data-ttu-id="b580a-103">Rimuove un certificato radice attendibile da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b580a-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="b580a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b580a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b580a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b580a-105">DESCRIPTION</span></span>
<span data-ttu-id="b580a-106">Il cmdlet **Remove-AzApplicationGatewayTrustedRootCertificate** rimuove un certificato radice attendibile da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="b580a-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="b580a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b580a-107">EXAMPLES</span></span>

### <span data-ttu-id="b580a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b580a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b580a-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $gw.</span><span class="sxs-lookup"><span data-stu-id="b580a-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="b580a-110">Il secondo comando rimuove il certificato radice attendibile denominato myRootCA dal gateway dell'applicazione archiviato in $gw.</span><span class="sxs-lookup"><span data-stu-id="b580a-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="b580a-111">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="b580a-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b580a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b580a-112">PARAMETERS</span></span>

### <span data-ttu-id="b580a-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b580a-113">-ApplicationGateway</span></span>
<span data-ttu-id="b580a-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b580a-114">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b580a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b580a-115">-DefaultProfile</span></span>
<span data-ttu-id="b580a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b580a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b580a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b580a-117">-Name</span></span>
<span data-ttu-id="b580a-118">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="b580a-118">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b580a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b580a-119">-Confirm</span></span>
<span data-ttu-id="b580a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b580a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b580a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b580a-121">-WhatIf</span></span>
<span data-ttu-id="b580a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b580a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b580a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b580a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b580a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b580a-124">CommonParameters</span></span>
<span data-ttu-id="b580a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b580a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b580a-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b580a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b580a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b580a-127">INPUTS</span></span>

### <span data-ttu-id="b580a-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b580a-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b580a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b580a-129">OUTPUTS</span></span>

### <span data-ttu-id="b580a-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b580a-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b580a-131">Note</span><span class="sxs-lookup"><span data-stu-id="b580a-131">NOTES</span></span>

## <span data-ttu-id="b580a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b580a-132">RELATED LINKS</span></span>

[<span data-ttu-id="b580a-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b580a-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b580a-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b580a-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b580a-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b580a-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="b580a-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b580a-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
