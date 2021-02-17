---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180663"
---
# <span data-ttu-id="e388d-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="e388d-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="e388d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e388d-102">SYNOPSIS</span></span>
<span data-ttu-id="e388d-103">Creare un oggetto PSHealthProbeSetting per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="e388d-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="e388d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e388d-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e388d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e388d-105">DESCRIPTION</span></span>
<span data-ttu-id="e388d-106">Creare un oggetto PSHealthProbeSetting per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="e388d-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="e388d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e388d-107">EXAMPLES</span></span>

### <span data-ttu-id="e388d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e388d-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="e388d-109">Nota: l'impostazione HealthProbeMethod non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e388d-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="e388d-110">Creare un oggetto PSHealthProbeSetting per la creazione di Front Door</span><span class="sxs-lookup"><span data-stu-id="e388d-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="e388d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e388d-111">PARAMETERS</span></span>

### <span data-ttu-id="e388d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e388d-112">-DefaultProfile</span></span>
<span data-ttu-id="e388d-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e388d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e388d-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e388d-114">-EnabledState</span></span>
<span data-ttu-id="e388d-115">Se abilitare o meno i back-end definiti in BackendPools.</span><span class="sxs-lookup"><span data-stu-id="e388d-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="e388d-116">I servizi di integrità possono essere disabilitati solo se è presente un singolo back-end abilitato in un singolo pool back-end abilitato.</span><span class="sxs-lookup"><span data-stu-id="e388d-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="e388d-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="e388d-117">-HealthProbeMethod</span></span>
<span data-ttu-id="e388d-118">Configura il metodo HTTP da usare per i back-end definiti in BackendPools.</span><span class="sxs-lookup"><span data-stu-id="e388d-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e388d-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e388d-119">-IntervalInSeconds</span></span>
<span data-ttu-id="e388d-120">Il numero di secondi tra l'integrità.</span><span class="sxs-lookup"><span data-stu-id="e388d-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="e388d-121">Il valore predefinito è 30</span><span class="sxs-lookup"><span data-stu-id="e388d-121">Default value is 30</span></span>

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

### <span data-ttu-id="e388d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e388d-122">-Name</span></span>
<span data-ttu-id="e388d-123">Nome dell'impostazione integrità.</span><span class="sxs-lookup"><span data-stu-id="e388d-123">Health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e388d-124">-Path</span><span class="sxs-lookup"><span data-stu-id="e388d-124">-Path</span></span>
<span data-ttu-id="e388d-125">Percorso da usare per l'integrità.</span><span class="sxs-lookup"><span data-stu-id="e388d-125">The path to use for the health probe.</span></span>
<span data-ttu-id="e388d-126">L'impostazione predefinita è /</span><span class="sxs-lookup"><span data-stu-id="e388d-126">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e388d-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e388d-127">-Protocol</span></span>
<span data-ttu-id="e388d-128">Schema protocollo da usare per questo valore predefinito predefinito è HTTP</span><span class="sxs-lookup"><span data-stu-id="e388d-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e388d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e388d-129">CommonParameters</span></span>
<span data-ttu-id="e388d-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e388d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e388d-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e388d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e388d-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e388d-132">INPUTS</span></span>

### <span data-ttu-id="e388d-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e388d-133">None</span></span>
## <span data-ttu-id="e388d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e388d-134">OUTPUTS</span></span>

### <span data-ttu-id="e388d-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="e388d-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="e388d-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e388d-136">NOTES</span></span>

## <span data-ttu-id="e388d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e388d-137">RELATED LINKS</span></span>

<span data-ttu-id="e388d-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="e388d-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
