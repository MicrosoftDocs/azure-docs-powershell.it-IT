---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336568"
---
# <span data-ttu-id="86797-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="86797-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="86797-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86797-102">SYNOPSIS</span></span>
<span data-ttu-id="86797-103">Modifica la catena di certificati CA del client attendibile di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86797-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="86797-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86797-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86797-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86797-105">DESCRIPTION</span></span>
<span data-ttu-id="86797-106">Il cmdlet **set-AzApplicationGatewayTrustedClientCertificate** modifica la catena di certificati CA client attendibili di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="86797-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="86797-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86797-107">EXAMPLES</span></span>

### <span data-ttu-id="86797-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="86797-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="86797-109">In scenari precedenti viene illustrato come aggiornare un oggetto della catena di certificati CA del client attendibile esistente.</span><span class="sxs-lookup"><span data-stu-id="86797-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="86797-110">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $gw.</span><span class="sxs-lookup"><span data-stu-id="86797-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="86797-111">Il secondo comando consente di modificare l'oggetto esistente della catena di certificati CA del client attendibile con un nuovo file della catena di certificati CA.</span><span class="sxs-lookup"><span data-stu-id="86797-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="86797-112">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="86797-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="86797-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86797-113">PARAMETERS</span></span>

### <span data-ttu-id="86797-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86797-114">-ApplicationGateway</span></span>
<span data-ttu-id="86797-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86797-115">The applicationGateway</span></span>

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

### <span data-ttu-id="86797-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="86797-116">-CertificateFile</span></span>
<span data-ttu-id="86797-117">Percorso del file della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="86797-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="86797-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86797-118">-DefaultProfile</span></span>
<span data-ttu-id="86797-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="86797-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86797-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="86797-120">-Name</span></span>
<span data-ttu-id="86797-121">Nome della catena di certificati CA del client attendibile</span><span class="sxs-lookup"><span data-stu-id="86797-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="86797-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="86797-122">-Confirm</span></span>
<span data-ttu-id="86797-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86797-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86797-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86797-124">-WhatIf</span></span>
<span data-ttu-id="86797-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86797-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86797-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86797-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86797-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86797-127">CommonParameters</span></span>
<span data-ttu-id="86797-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86797-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86797-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86797-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86797-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86797-130">INPUTS</span></span>

### <span data-ttu-id="86797-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86797-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="86797-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86797-132">OUTPUTS</span></span>

### <span data-ttu-id="86797-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="86797-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="86797-134">Note</span><span class="sxs-lookup"><span data-stu-id="86797-134">NOTES</span></span>

## <span data-ttu-id="86797-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86797-135">RELATED LINKS</span></span>

[<span data-ttu-id="86797-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="86797-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="86797-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="86797-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="86797-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="86797-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="86797-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="86797-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)