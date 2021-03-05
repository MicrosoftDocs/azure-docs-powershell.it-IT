---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: c458973a5cff000cab13c4602e1a73234314c0d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963294"
---
# <span data-ttu-id="29202-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="29202-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="29202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29202-102">SYNOPSIS</span></span>
<span data-ttu-id="29202-103">Ottiene l'URL Single #A0 di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="29202-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="29202-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29202-104">SYNTAX</span></span>

### <span data-ttu-id="29202-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29202-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29202-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29202-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29202-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29202-107">DESCRIPTION</span></span>
<span data-ttu-id="29202-108">Il cmdlet **Get-AzCdnProfileSsoUrl** ottiene l'URL Single #A0 del profilo della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="29202-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="29202-109">Questo URL consente agli utenti di connettersi a un portale supplementare e usare caratteristiche aggiuntive della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="29202-109">This URL lets users connect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="29202-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29202-110">EXAMPLES</span></span>

## <span data-ttu-id="29202-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29202-111">PARAMETERS</span></span>

### <span data-ttu-id="29202-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="29202-112">-CdnProfile</span></span>
<span data-ttu-id="29202-113">Specifica il profilo della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="29202-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="29202-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29202-114">-DefaultProfile</span></span>
<span data-ttu-id="29202-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="29202-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29202-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="29202-116">-ProfileName</span></span>
<span data-ttu-id="29202-117">Specifica il nome del profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="29202-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="29202-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29202-118">-ResourceGroupName</span></span>
<span data-ttu-id="29202-119">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="29202-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="29202-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29202-120">CommonParameters</span></span>
<span data-ttu-id="29202-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29202-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29202-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29202-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29202-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="29202-123">INPUTS</span></span>

### <span data-ttu-id="29202-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="29202-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="29202-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29202-125">OUTPUTS</span></span>

### <span data-ttu-id="29202-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="29202-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="29202-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="29202-127">NOTES</span></span>

## <span data-ttu-id="29202-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29202-128">RELATED LINKS</span></span>

[<span data-ttu-id="29202-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="29202-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


