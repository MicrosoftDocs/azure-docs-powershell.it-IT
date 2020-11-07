---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 93D5E2D9-FB89-4311-8E8E-44CBFAFC98A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilessourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSsoUrl.md
ms.openlocfilehash: 64e9c4bc8f279858c4c889c00eee058aab0cad4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852262"
---
# <span data-ttu-id="2cc33-101">Get-AzCdnProfileSsoUrl</span><span class="sxs-lookup"><span data-stu-id="2cc33-101">Get-AzCdnProfileSsoUrl</span></span>

## <span data-ttu-id="2cc33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cc33-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc33-103">Ottiene l'URL Single Sign-on di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="2cc33-103">Gets the single sign-on URL of a CDN profile.</span></span>

## <span data-ttu-id="2cc33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cc33-104">SYNTAX</span></span>

### <span data-ttu-id="2cc33-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cc33-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSsoUrl -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc33-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cc33-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSsoUrl -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc33-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cc33-107">DESCRIPTION</span></span>
<span data-ttu-id="2cc33-108">Il cmdlet **Get-AzCdnProfileSsoUrl** Ottiene l'URL Single Sign-on del profilo della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="2cc33-108">The **Get-AzCdnProfileSsoUrl** cmdlet gets the single sign-on URL of the Azure Content Delivery Network (CDN) profile.</span></span>
<span data-ttu-id="2cc33-109">Questo URL consente agli utenti di Conntect a un portale aggiuntivo e di usare le funzionalità aggiuntive della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="2cc33-109">This URL lets users conntect to a supplementary portal and use additional features of  CDN.</span></span>

## <span data-ttu-id="2cc33-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cc33-110">EXAMPLES</span></span>

## <span data-ttu-id="2cc33-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cc33-111">PARAMETERS</span></span>

### <span data-ttu-id="2cc33-112">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2cc33-112">-CdnProfile</span></span>
<span data-ttu-id="2cc33-113">Specifica il profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="2cc33-113">Specifies the CDN profile.</span></span>

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

### <span data-ttu-id="2cc33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc33-114">-DefaultProfile</span></span>
<span data-ttu-id="2cc33-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2cc33-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cc33-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2cc33-116">-ProfileName</span></span>
<span data-ttu-id="2cc33-117">Specifica il nome del profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="2cc33-117">Specifies the name of the CDN profile.</span></span>

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

### <span data-ttu-id="2cc33-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc33-118">-ResourceGroupName</span></span>
<span data-ttu-id="2cc33-119">Specifica il nome del nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="2cc33-119">Specifies the name of the resource group name to which the profile belongs.</span></span>

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

### <span data-ttu-id="2cc33-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc33-120">CommonParameters</span></span>
<span data-ttu-id="2cc33-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cc33-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc33-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cc33-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc33-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cc33-123">INPUTS</span></span>

### <span data-ttu-id="2cc33-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="2cc33-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2cc33-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cc33-125">OUTPUTS</span></span>

### <span data-ttu-id="2cc33-126">Microsoft. Azure. Commands. CDN. Models. profile. PSSsoUri</span><span class="sxs-lookup"><span data-stu-id="2cc33-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSSsoUri</span></span>

## <span data-ttu-id="2cc33-127">Note</span><span class="sxs-lookup"><span data-stu-id="2cc33-127">NOTES</span></span>

## <span data-ttu-id="2cc33-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cc33-128">RELATED LINKS</span></span>

[<span data-ttu-id="2cc33-129">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="2cc33-129">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)


