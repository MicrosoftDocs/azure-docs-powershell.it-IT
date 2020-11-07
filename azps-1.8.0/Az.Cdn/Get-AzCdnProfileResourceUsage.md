---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: d33cc54102d06b3bd57784880280b6e035fce18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684873"
---
# <span data-ttu-id="0c13d-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="0c13d-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="0c13d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c13d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c13d-103">Ottiene l'utilizzo delle risorse di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="0c13d-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="0c13d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c13d-104">SYNTAX</span></span>

### <span data-ttu-id="0c13d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c13d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c13d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c13d-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c13d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c13d-107">DESCRIPTION</span></span>
<span data-ttu-id="0c13d-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="0c13d-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="0c13d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c13d-109">EXAMPLES</span></span>

### <span data-ttu-id="0c13d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c13d-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0c13d-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="0c13d-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="0c13d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c13d-112">PARAMETERS</span></span>

### <span data-ttu-id="0c13d-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="0c13d-113">-CdnProfile</span></span>
<span data-ttu-id="0c13d-114">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="0c13d-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="0c13d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c13d-115">-DefaultProfile</span></span>
<span data-ttu-id="0c13d-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c13d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c13d-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0c13d-117">-ProfileName</span></span>
<span data-ttu-id="0c13d-118">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="0c13d-118">The name of the profile.</span></span>

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

### <span data-ttu-id="0c13d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c13d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c13d-120">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="0c13d-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="0c13d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c13d-121">CommonParameters</span></span>
<span data-ttu-id="0c13d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c13d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c13d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c13d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c13d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c13d-124">INPUTS</span></span>

### <span data-ttu-id="0c13d-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="0c13d-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="0c13d-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c13d-126">OUTPUTS</span></span>

### <span data-ttu-id="0c13d-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="0c13d-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="0c13d-128">Note</span><span class="sxs-lookup"><span data-stu-id="0c13d-128">NOTES</span></span>

## <span data-ttu-id="0c13d-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c13d-129">RELATED LINKS</span></span>