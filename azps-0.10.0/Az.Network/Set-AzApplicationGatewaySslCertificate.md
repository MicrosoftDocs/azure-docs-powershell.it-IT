---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862818"
---
# <span data-ttu-id="83d4d-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="83d4d-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="83d4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="83d4d-103">Imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="83d4d-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="83d4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83d4d-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83d4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83d4d-105">DESCRIPTION</span></span>
<span data-ttu-id="83d4d-106">Il cmdlet **set-AzApplicationGatewaySslCertificate** imposta lo stato obiettivo di un certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="83d4d-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="83d4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83d4d-107">EXAMPLES</span></span>

### <span data-ttu-id="83d4d-108">Esempio 1: impostare lo stato dell'obiettivo di un certificato SSL</span><span class="sxs-lookup"><span data-stu-id="83d4d-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="83d4d-109">Questo comando imposta lo stato dell'obiettivo di un certificato SSL dal gateway dell'applicazione denominato ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="83d4d-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="83d4d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83d4d-110">PARAMETERS</span></span>

### <span data-ttu-id="83d4d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="83d4d-111">-ApplicationGateway</span></span>
<span data-ttu-id="83d4d-112">Specifica il gateway dell'applicazione a cui è associato il certificato SSL (Secure Socket Layer).</span><span class="sxs-lookup"><span data-stu-id="83d4d-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="83d4d-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="83d4d-113">-CertificateFile</span></span>
<span data-ttu-id="83d4d-114">Specifica il percorso del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="83d4d-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="83d4d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d4d-115">-DefaultProfile</span></span>
<span data-ttu-id="83d4d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83d4d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d4d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="83d4d-117">-Name</span></span>
<span data-ttu-id="83d4d-118">Specifica il nome del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="83d4d-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="83d4d-119">-Password</span><span class="sxs-lookup"><span data-stu-id="83d4d-119">-Password</span></span>
<span data-ttu-id="83d4d-120">Specifica la password del certificato SSL.</span><span class="sxs-lookup"><span data-stu-id="83d4d-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83d4d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d4d-121">CommonParameters</span></span>
<span data-ttu-id="83d4d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d4d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d4d-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d4d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d4d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83d4d-124">INPUTS</span></span>

### <span data-ttu-id="83d4d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="83d4d-125">System.String</span></span>

## <span data-ttu-id="83d4d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83d4d-126">OUTPUTS</span></span>

### <span data-ttu-id="83d4d-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="83d4d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="83d4d-128">Note</span><span class="sxs-lookup"><span data-stu-id="83d4d-128">NOTES</span></span>

## <span data-ttu-id="83d4d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83d4d-129">RELATED LINKS</span></span>

[<span data-ttu-id="83d4d-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="83d4d-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="83d4d-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="83d4d-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="83d4d-132">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="83d4d-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="83d4d-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="83d4d-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


