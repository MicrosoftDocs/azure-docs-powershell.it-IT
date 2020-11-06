---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSsoUrl.md
ms.openlocfilehash: 3ad44ba1edcec844dcb542defb1baf294aeaa89b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509299"
---
# <span data-ttu-id="f8782-101">Get-AzureRmCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="f8782-101">Get-AzureRmCdnProfileSsoUrl</span></span>

## <span data-ttu-id="f8782-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8782-102">SYNOPSIS</span></span>
<span data-ttu-id="f8782-103">Ottiene l'URL Single Sign-on di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="f8782-103">Gets the single sign-on URL of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8782-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8782-104">SYNTAX</span></span>

### <span data-ttu-id="f8782-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8782-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8782-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8782-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8782-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8782-107">DESCRIPTION</span></span>
<span data-ttu-id="f8782-108">Il cmdlet **Get-AzureRmCdnProfileSsoUrl** Ottiene l'URL Single Sign-on del profilo della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="f8782-108">The **Get-AzureRmCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="f8782-109">Questo URL consente agli utenti di Conntect a un portale aggiuntivo e di usare le funzionalità aggiuntive della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="f8782-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="f8782-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8782-110">EXAMPLES</span></span>

## <span data-ttu-id="f8782-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8782-111">PARAMETERS</span></span>

### <span data-ttu-id="f8782-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8782-112">-CdnProfile</span></span>
<span data-ttu-id="f8782-113">Specifica il profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="f8782-113">Specifies the CDN profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8782-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8782-114">-DefaultProfile</span></span>
<span data-ttu-id="f8782-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f8782-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8782-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f8782-116">-ProfileName</span></span>
<span data-ttu-id="f8782-117">Specifica il nome del profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="f8782-117">Specifies the name of the CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8782-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8782-118">-ResourceGroupName</span></span>
<span data-ttu-id="f8782-119">Specifica il nome del nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="f8782-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8782-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8782-120">CommonParameters</span></span>
<span data-ttu-id="f8782-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8782-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8782-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8782-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8782-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8782-123">INPUTS</span></span>

### <span data-ttu-id="f8782-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f8782-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="f8782-125">Parametri: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8782-125">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="f8782-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8782-126">OUTPUTS</span></span>

### <span data-ttu-id="f8782-127">Microsoft. Azure. Commands. CDN. Models. profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="f8782-127">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="f8782-128">Note</span><span class="sxs-lookup"><span data-stu-id="f8782-128">NOTES</span></span>

## <span data-ttu-id="f8782-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8782-129">RELATED LINKS</span></span>

[<span data-ttu-id="f8782-130">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f8782-130">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)


