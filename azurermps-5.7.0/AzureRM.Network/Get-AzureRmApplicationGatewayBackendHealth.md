---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D5E928C3-26B6-4B7C-8A9C-F1F602BABF75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaybackendhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayBackendHealth.md
ms.openlocfilehash: 6e6a2bef9ea6bc237db97139bcc7e9e7a0624fd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509832"
---
# <span data-ttu-id="33c5d-101">Get-AzureRmApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="33c5d-101">Get-AzureRmApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="33c5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="33c5d-103">Ottiene l'integrità del backend di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="33c5d-103">Gets application gateway backend health.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33c5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33c5d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayBackendHealth -Name <String> -ResourceGroupName <String>
 [-ExpandResource <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33c5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="33c5d-106">Il cmdlet Get-AzureRmApplicationGatewayBackendHealth Ottiene l'integrità del backend di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="33c5d-106">The Get-AzureRmApplicationGatewayBackendHealth cmdlet gets application gateway backend health.</span></span>

## <span data-ttu-id="33c5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33c5d-107">EXAMPLES</span></span>

### <span data-ttu-id="33c5d-108">--------------------------Esempio 1: Ottiene l'integrità del backend senza risorse espanse.</span><span class="sxs-lookup"><span data-stu-id="33c5d-108">--------------------------  Example 1: Gets backend health without expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="33c5d-109">Questo comando consente di ottenere lo stato di integrità del gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="33c5d-109">This command gets the backend health of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

### <span data-ttu-id="33c5d-110">--------------------------Esempio 1: Ottiene l'integrità del backend con risorse espanse.</span><span class="sxs-lookup"><span data-stu-id="33c5d-110">--------------------------  Example 1: Gets backend health with expanded resources.</span></span>  --------------------------
```
PS C:\>$BackendHealth = Get-AzureRmApplicationGatewayBackendHealth -Name ApplicationGateway01 -ResourceGroupName ResourceGroup01 -ExpandResource "backendhealth/applicationgatewayresource"
```

<span data-ttu-id="33c5d-111">Questo comando consente di ottenere lo stato di back-end (con risorse espanse) del gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $BackendHealth.</span><span class="sxs-lookup"><span data-stu-id="33c5d-111">This command gets the backend health (with expanded resources) of application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $BackendHealth variable.</span></span>

## <span data-ttu-id="33c5d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33c5d-112">PARAMETERS</span></span>

### <span data-ttu-id="33c5d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33c5d-113">-AsJob</span></span>
<span data-ttu-id="33c5d-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="33c5d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33c5d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c5d-115">-DefaultProfile</span></span>
<span data-ttu-id="33c5d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33c5d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33c5d-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="33c5d-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c5d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="33c5d-118">-Name</span></span>
<span data-ttu-id="33c5d-119">Specifica il nome del gateway dell'applicazione ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c5d-119">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c5d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c5d-120">-ResourceGroupName</span></span>
<span data-ttu-id="33c5d-121">Specifica il nome del gruppo di risorse che contiene il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33c5d-121">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c5d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c5d-122">CommonParameters</span></span>
<span data-ttu-id="33c5d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c5d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c5d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33c5d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c5d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33c5d-125">INPUTS</span></span>

### <span data-ttu-id="33c5d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="33c5d-126">System.String</span></span>

## <span data-ttu-id="33c5d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33c5d-127">OUTPUTS</span></span>

### <span data-ttu-id="33c5d-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHealth</span><span class="sxs-lookup"><span data-stu-id="33c5d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHealth</span></span>

## <span data-ttu-id="33c5d-129">Note</span><span class="sxs-lookup"><span data-stu-id="33c5d-129">NOTES</span></span>
<span data-ttu-id="33c5d-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="33c5d-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="33c5d-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33c5d-131">RELATED LINKS</span></span>

[<span data-ttu-id="33c5d-132">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="33c5d-132">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

