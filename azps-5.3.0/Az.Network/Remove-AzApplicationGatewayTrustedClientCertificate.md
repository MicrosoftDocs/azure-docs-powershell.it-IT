---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486683"
---
# <span data-ttu-id="5e230-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5e230-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="5e230-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e230-102">SYNOPSIS</span></span>
<span data-ttu-id="5e230-103">Rimuove l'oggetto della catena di certificati CA client attendibile da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e230-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="5e230-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e230-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e230-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e230-105">DESCRIPTION</span></span>
<span data-ttu-id="5e230-106">Il cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** rimuove l'oggetto della catena di certificati CA del client attendibile da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5e230-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="5e230-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e230-107">EXAMPLES</span></span>

### <span data-ttu-id="5e230-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e230-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="5e230-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $gw.</span><span class="sxs-lookup"><span data-stu-id="5e230-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="5e230-110">Il secondo comando rimuove la catena di certificati CA client attendibile denominata "TrustedClientCertificate01" dal gateway dell'applicazione archiviato in $gw.</span><span class="sxs-lookup"><span data-stu-id="5e230-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="5e230-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e230-111">PARAMETERS</span></span>

### <span data-ttu-id="5e230-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e230-112">-ApplicationGateway</span></span>
<span data-ttu-id="5e230-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e230-113">The applicationGateway</span></span>

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

### <span data-ttu-id="5e230-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e230-114">-DefaultProfile</span></span>
<span data-ttu-id="5e230-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e230-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e230-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e230-116">-Name</span></span>
<span data-ttu-id="5e230-117">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="5e230-117">The name of the trusted client CA certificate chain</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e230-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e230-118">-Confirm</span></span>
<span data-ttu-id="5e230-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e230-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e230-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e230-120">-WhatIf</span></span>
<span data-ttu-id="5e230-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e230-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e230-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e230-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e230-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e230-123">CommonParameters</span></span>
<span data-ttu-id="5e230-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e230-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e230-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e230-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e230-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e230-126">INPUTS</span></span>

### <span data-ttu-id="5e230-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e230-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e230-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e230-128">OUTPUTS</span></span>

### <span data-ttu-id="5e230-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5e230-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5e230-130">Note</span><span class="sxs-lookup"><span data-stu-id="5e230-130">NOTES</span></span>

## <span data-ttu-id="5e230-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e230-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e230-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5e230-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="5e230-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5e230-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="5e230-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5e230-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="5e230-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="5e230-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)