---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 2365502bb681cafe8ed7fedb05a4a862e54a3cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686866"
---
# <span data-ttu-id="dabac-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="dabac-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="dabac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dabac-102">SYNOPSIS</span></span>
<span data-ttu-id="dabac-103">Ottiene l'URL Single Sign-on di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="dabac-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dabac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dabac-104">SYNTAX</span></span>

### <span data-ttu-id="dabac-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dabac-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dabac-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="dabac-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dabac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dabac-107">DESCRIPTION</span></span>
<span data-ttu-id="dabac-108">Il cmdlet **Get-AzureRmCdnProfileSsoUrl** Ottiene l'URL Single Sign-on del profilo della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="dabac-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="dabac-109">Questo URL consente agli utenti di Conntect a un portale aggiuntivo e di usare le funzionalità aggiuntive della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="dabac-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="dabac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dabac-110">EXAMPLES</span></span>

## <span data-ttu-id="dabac-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dabac-111">PARAMETERS</span></span>

### <span data-ttu-id="dabac-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="dabac-112">-CdnProfile</span></span>
<span data-ttu-id="dabac-113">Specifica il profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="dabac-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dabac-114">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dabac-114">-ProfileName</span></span>
<span data-ttu-id="dabac-115">Specifica il nome del profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="dabac-115">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabac-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabac-116">-ResourceGroupName</span></span>
<span data-ttu-id="dabac-117">Specifica il nome del nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="dabac-117">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabac-118">-DefaultProfile</span></span>
<span data-ttu-id="dabac-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dabac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabac-120">CommonParameters</span></span>
<span data-ttu-id="dabac-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabac-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabac-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dabac-123">INPUTS</span></span>

### <span data-ttu-id="dabac-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="dabac-124">PSProfile</span></span>
<span data-ttu-id="dabac-125">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dabac-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="dabac-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dabac-126">OUTPUTS</span></span>

###  
<span data-ttu-id="dabac-127">Questo cmdlet restituisce un URL.</span><span class="sxs-lookup"><span data-stu-id="dabac-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="dabac-128">Note</span><span class="sxs-lookup"><span data-stu-id="dabac-128">NOTES</span></span>

## <span data-ttu-id="dabac-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dabac-129">RELATED LINKS</span></span>

[<span data-ttu-id="dabac-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="dabac-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


