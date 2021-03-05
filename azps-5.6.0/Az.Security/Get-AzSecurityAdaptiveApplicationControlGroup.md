---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: c23c04a5a9df3464bd84a2261435c744374cfb3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011726"
---
# <span data-ttu-id="1e2c3-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="1e2c3-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="1e2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2c3-103">Ottiene un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="1e2c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e2c3-104">SYNTAX</span></span>

### <span data-ttu-id="1e2c3-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e2c3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e2c3-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e2c3-106">DESCRIPTION</span></span>
<span data-ttu-id="1e2c3-107">I controlli adattivi delle applicazioni vengono calcolati automaticamente dal Centro sicurezza di Azure e usano questo cmdlet per ottenere un gruppo di server/macchina virtuale di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="1e2c3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e2c3-108">EXAMPLES</span></span>

### <span data-ttu-id="1e2c3-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e2c3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="1e2c3-110">Ottiene un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="1e2c3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e2c3-111">PARAMETERS</span></span>

### <span data-ttu-id="1e2c3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2c3-112">-DefaultProfile</span></span>
<span data-ttu-id="1e2c3-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e2c3-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="1e2c3-114">-AscLocation</span></span>
<span data-ttu-id="1e2c3-115">Posizione in cui asc archivia i dati della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="1e2c3-116">possono essere recuperate da Ottieni posizioni.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c3-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="1e2c3-117">-GroupName</span></span>
<span data-ttu-id="1e2c3-118">Nome di un gruppo di server/vm di controllo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e2c3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e2c3-119">-SubscriptionId</span></span>
<span data-ttu-id="1e2c3-120">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="1e2c3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2c3-121">CommonParameters</span></span>
<span data-ttu-id="1e2c3-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e2c3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2c3-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e2c3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2c3-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e2c3-124">INPUTS</span></span>

### <span data-ttu-id="1e2c3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1e2c3-125">System.String</span></span>

## <span data-ttu-id="1e2c3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e2c3-126">OUTPUTS</span></span>

### <span data-ttu-id="1e2c3-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplication Più.PsSecurityAdaptiveApplicationApplication</span><span class="sxs-lookup"><span data-stu-id="1e2c3-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="1e2c3-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e2c3-128">NOTES</span></span>

## <span data-ttu-id="1e2c3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e2c3-129">RELATED LINKS</span></span>