---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: c61c39bc95ae3521d7b0b573c43e303749999cbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971086"
---
# <span data-ttu-id="55824-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="55824-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="55824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55824-102">SYNOPSIS</span></span>
<span data-ttu-id="55824-103">Creare un oggetto PSBackendPoolsSetting per la creazione di Front Door.</span><span class="sxs-lookup"><span data-stu-id="55824-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="55824-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55824-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55824-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="55824-105">DESCRIPTION</span></span>
<span data-ttu-id="55824-106">Il cmdlet **New-AzFrontDoorBackendpoolsSettingObject** crea un nuovo oggetto PSBackendPoolsSettings per la creazione della porta anteriore.</span><span class="sxs-lookup"><span data-stu-id="55824-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="55824-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55824-107">EXAMPLES</span></span>

### <span data-ttu-id="55824-108">Esempio 1: Creare l'oggetto BackendPoolsSettings usando i valori predefiniti</span><span class="sxs-lookup"><span data-stu-id="55824-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="55824-109">Esempio 2: Creare l'oggetto BackendPoolsSettings con i valori specificati dall'utente</span><span class="sxs-lookup"><span data-stu-id="55824-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="55824-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55824-110">PARAMETERS</span></span>

### <span data-ttu-id="55824-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55824-111">-DefaultProfile</span></span>
<span data-ttu-id="55824-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55824-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55824-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="55824-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="55824-114">Se applicare o meno la verifica del nome del certificato nelle richieste HTTPS a tutti i pool back-end.</span><span class="sxs-lookup"><span data-stu-id="55824-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="55824-115">Nessun effetto sulle richieste non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="55824-115">No effect on non-HTTPS requests.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55824-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="55824-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="55824-117">Timeout di invio e ricezione durante la richiesta di inoltro al back-end.</span><span class="sxs-lookup"><span data-stu-id="55824-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="55824-118">Quando viene raggiunto il timeout, la richiesta non riesce e restituisce.</span><span class="sxs-lookup"><span data-stu-id="55824-118">When timeout is reached, the request fails and returns.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55824-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55824-119">CommonParameters</span></span>
<span data-ttu-id="55824-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55824-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55824-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="55824-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55824-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="55824-122">INPUTS</span></span>

### <span data-ttu-id="55824-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="55824-123">None</span></span>

## <span data-ttu-id="55824-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55824-124">OUTPUTS</span></span>

### <span data-ttu-id="55824-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="55824-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="55824-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="55824-126">NOTES</span></span>

## <span data-ttu-id="55824-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55824-127">RELATED LINKS</span></span>
