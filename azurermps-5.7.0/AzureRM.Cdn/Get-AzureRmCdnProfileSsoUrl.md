---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: d93dadc062f2cc12ed363039d69266daf365920e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510064"
---
# <span data-ttu-id="fe3fd-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="fe3fd-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="fe3fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3fd-103">Ottiene l'URL Single Sign-on di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe3fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe3fd-104">SYNTAX</span></span>

### <span data-ttu-id="fe3fd-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fe3fd-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe3fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3fd-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe3fd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe3fd-107">DESCRIPTION</span></span>
<span data-ttu-id="fe3fd-108">Il cmdlet **Get-AzureRmCdnProfileSsoUrl** Ottiene l'URL Single Sign-on del profilo della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="fe3fd-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="fe3fd-109">Questo URL consente agli utenti di Conntect a un portale aggiuntivo e di usare le funzionalità aggiuntive della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="fe3fd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe3fd-110">EXAMPLES</span></span>

## <span data-ttu-id="fe3fd-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe3fd-111">PARAMETERS</span></span>

### <span data-ttu-id="fe3fd-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="fe3fd-112">-CdnProfile</span></span>
<span data-ttu-id="fe3fd-113">Specifica il profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-113">Specifies the CDN profile.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3fd-114">-DefaultProfile</span></span>
<span data-ttu-id="fe3fd-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe3fd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe3fd-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fe3fd-116">-ProfileName</span></span>
<span data-ttu-id="fe3fd-117">Specifica il nome del profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3fd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe3fd-118">-ResourceGroupName</span></span>
<span data-ttu-id="fe3fd-119">Specifica il nome del nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3fd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3fd-120">CommonParameters</span></span>
<span data-ttu-id="fe3fd-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3fd-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3fd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3fd-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe3fd-123">INPUTS</span></span>

### <span data-ttu-id="fe3fd-124">PSProfile</span><span class="sxs-lookup"><span data-stu-id="fe3fd-124">PSProfile</span></span>
<span data-ttu-id="fe3fd-125">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fe3fd-125">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="fe3fd-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe3fd-126">OUTPUTS</span></span>

###  
<span data-ttu-id="fe3fd-127">Questo cmdlet restituisce un URL.</span><span class="sxs-lookup"><span data-stu-id="fe3fd-127">This cmdlet returns a URL.</span></span>

## <span data-ttu-id="fe3fd-128">Note</span><span class="sxs-lookup"><span data-stu-id="fe3fd-128">NOTES</span></span>

## <span data-ttu-id="fe3fd-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe3fd-129">RELATED LINKS</span></span>

[<span data-ttu-id="fe3fd-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fe3fd-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


