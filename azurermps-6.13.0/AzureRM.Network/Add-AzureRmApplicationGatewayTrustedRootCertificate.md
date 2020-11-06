---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520181"
---
# <span data-ttu-id="d7bcd-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d7bcd-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d7bcd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d7bcd-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bcd-103">Aggiunge un certificato radice attendibile a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7bcd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7bcd-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7bcd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7bcd-105">DESCRIPTION</span></span>
<span data-ttu-id="d7bcd-106">Il cmdlet **Add-AzureRmApplicationGatewayTrustedRootCertificate** aggiunge un certificato radice attendibile a un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="d7bcd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7bcd-107">EXAMPLES</span></span>

### <span data-ttu-id="d7bcd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7bcd-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d7bcd-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d7bcd-110">Il secondo comando addes un nuovo certificato radice attendibile al gateway dell'applicazione che prende il percorso del certificato radice come input.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="d7bcd-111">Il terzo comando crea una nuova impostazione http backend usando il certificato radice attendibile per la convalida del certificato del server back-end.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="d7bcd-112">Il comando quarto aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="d7bcd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d7bcd-113">PARAMETERS</span></span>

### <span data-ttu-id="d7bcd-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7bcd-114">-ApplicationGateway</span></span>
<span data-ttu-id="d7bcd-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7bcd-115">The applicationGateway</span></span>

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

### <span data-ttu-id="d7bcd-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d7bcd-116">-CertificateFile</span></span>
<span data-ttu-id="d7bcd-117">Percorso del file CER certificato</span><span class="sxs-lookup"><span data-stu-id="d7bcd-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="d7bcd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bcd-118">-DefaultProfile</span></span>
<span data-ttu-id="d7bcd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bcd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7bcd-120">-Name</span></span>
<span data-ttu-id="d7bcd-121">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="d7bcd-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d7bcd-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d7bcd-122">-Confirm</span></span>
<span data-ttu-id="d7bcd-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7bcd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7bcd-124">-WhatIf</span></span>
<span data-ttu-id="d7bcd-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7bcd-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7bcd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bcd-127">CommonParameters</span></span>
<span data-ttu-id="d7bcd-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bcd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bcd-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7bcd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bcd-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d7bcd-130">INPUTS</span></span>

### <span data-ttu-id="d7bcd-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7bcd-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7bcd-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7bcd-132">OUTPUTS</span></span>

### <span data-ttu-id="d7bcd-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d7bcd-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d7bcd-134">Note</span><span class="sxs-lookup"><span data-stu-id="d7bcd-134">NOTES</span></span>

## <span data-ttu-id="d7bcd-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7bcd-135">RELATED LINKS</span></span>
