---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: eecce510632e7eef3fc61cf53127777b93c81e51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513647"
---
# <span data-ttu-id="c27a2-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c27a2-101">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="c27a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c27a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c27a2-103">Rimuove un certificato radice attendibile da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c27a2-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c27a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c27a2-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayTrustedRootCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c27a2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c27a2-105">DESCRIPTION</span></span>
<span data-ttu-id="c27a2-106">Il cmdlet **Remove-AzureRmApplicationGatewayTrustedRootCertificate** rimuove un certificato radice attendibile da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c27a2-106">The **Remove-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="c27a2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c27a2-107">EXAMPLES</span></span>

### <span data-ttu-id="c27a2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c27a2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="c27a2-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $gw.</span><span class="sxs-lookup"><span data-stu-id="c27a2-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="c27a2-110">Il secondo comando rimuove il certificato radice attendibile denominato myRootCA dal gateway dell'applicazione archiviato in $gw.</span><span class="sxs-lookup"><span data-stu-id="c27a2-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="c27a2-111">Il terzo comando Aggiorna il gateway dell'applicazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="c27a2-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="c27a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c27a2-112">PARAMETERS</span></span>

### <span data-ttu-id="c27a2-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c27a2-113">-ApplicationGateway</span></span>
<span data-ttu-id="c27a2-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c27a2-114">The applicationGateway</span></span>

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

### <span data-ttu-id="c27a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27a2-115">-DefaultProfile</span></span>
<span data-ttu-id="c27a2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c27a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c27a2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c27a2-117">-Name</span></span>
<span data-ttu-id="c27a2-118">Nome del certificato TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="c27a2-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="c27a2-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c27a2-119">-Confirm</span></span>
<span data-ttu-id="c27a2-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c27a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c27a2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c27a2-121">-WhatIf</span></span>
<span data-ttu-id="c27a2-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c27a2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c27a2-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c27a2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c27a2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27a2-124">CommonParameters</span></span>
<span data-ttu-id="c27a2-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c27a2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27a2-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c27a2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27a2-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c27a2-127">INPUTS</span></span>

### <span data-ttu-id="c27a2-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c27a2-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c27a2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c27a2-129">OUTPUTS</span></span>

### <span data-ttu-id="c27a2-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c27a2-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c27a2-131">Note</span><span class="sxs-lookup"><span data-stu-id="c27a2-131">NOTES</span></span>

## <span data-ttu-id="c27a2-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c27a2-132">RELATED LINKS</span></span>
