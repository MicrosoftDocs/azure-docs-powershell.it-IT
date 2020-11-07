---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 96872aa399c3241710e12e3b96a14e8678f21d83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860909"
---
# <span data-ttu-id="ed71c-101">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ed71c-101">Get-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="ed71c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed71c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed71c-103">Ottiene le impostazioni HTTP di back-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed71c-103">Gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="ed71c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed71c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayBackendHttpSetting [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed71c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed71c-105">DESCRIPTION</span></span>
<span data-ttu-id="ed71c-106">Il cmdlet Get-AzApplicationGatewayBackendHttpSetting ottiene le impostazioni HTTP di back-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed71c-106">The Get-AzApplicationGatewayBackendHttpSetting cmdlet gets the back-end HTTP settings of an application gateway.</span></span>

## <span data-ttu-id="ed71c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed71c-107">EXAMPLES</span></span>

### <span data-ttu-id="ed71c-108">Esempio 1: ottenere le impostazioni HTTP di back-end per nome</span><span class="sxs-lookup"><span data-stu-id="ed71c-108">Example 1: Get back-end HTTP settings by name</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSetting -Name "Settings01" -ApplicationGateway $AppGw
```

<span data-ttu-id="ed71c-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene le impostazioni HTTP denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings.</span><span class="sxs-lookup"><span data-stu-id="ed71c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>

### <span data-ttu-id="ed71c-110">Esempio 2: ottenere una raccolta di impostazioni HTTP di back-end</span><span class="sxs-lookup"><span data-stu-id="ed71c-110">Example 2: Get a collection of back-end HTTP settings</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SettingsList  = Get-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw
```

<span data-ttu-id="ed71c-111">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw. Il secondo comando ottiene la raccolta di impostazioni HTTP per $AppGw e archivia le impostazioni nella variabile $SettingsList.</span><span class="sxs-lookup"><span data-stu-id="ed71c-111">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the collection of HTTP settings for $AppGw and stores the settings in the $SettingsList variable.</span></span>

## <span data-ttu-id="ed71c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed71c-112">PARAMETERS</span></span>

### <span data-ttu-id="ed71c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed71c-113">-ApplicationGateway</span></span>
<span data-ttu-id="ed71c-114">Specifica un oggetto gateway dell'applicazione che contiene le impostazioni HTTP di back-end.</span><span class="sxs-lookup"><span data-stu-id="ed71c-114">Specifies an application gateway object that contains back-end HTTP settings.</span></span>

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

### <span data-ttu-id="ed71c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed71c-115">-DefaultProfile</span></span>
<span data-ttu-id="ed71c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed71c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed71c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed71c-117">-Name</span></span>
<span data-ttu-id="ed71c-118">Specifica il nome delle impostazioni HTTP di backend che questo cmdlet ottiene.</span><span class="sxs-lookup"><span data-stu-id="ed71c-118">Specifies the name of the backend HTTP settings that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed71c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed71c-119">CommonParameters</span></span>
<span data-ttu-id="ed71c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed71c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed71c-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed71c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed71c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed71c-122">INPUTS</span></span>

### <span data-ttu-id="ed71c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ed71c-123">System.String</span></span>

## <span data-ttu-id="ed71c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed71c-124">OUTPUTS</span></span>

### <span data-ttu-id="ed71c-125">Microsoft. Azure. Commands. Network. Models. AzureApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ed71c-125">Microsoft.Azure.Commands.Network.Models.AzureApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="ed71c-126">Note</span><span class="sxs-lookup"><span data-stu-id="ed71c-126">NOTES</span></span>

## <span data-ttu-id="ed71c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed71c-127">RELATED LINKS</span></span>

[<span data-ttu-id="ed71c-128">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ed71c-128">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="ed71c-129">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ed71c-129">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="ed71c-130">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ed71c-130">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="ed71c-131">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="ed71c-131">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

