---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473874"
---
# <span data-ttu-id="433c8-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="433c8-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="433c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="433c8-102">SYNOPSIS</span></span>
<span data-ttu-id="433c8-103">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="433c8-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="433c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="433c8-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433c8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="433c8-105">DESCRIPTION</span></span>
<span data-ttu-id="433c8-106">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="433c8-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="433c8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="433c8-107">EXAMPLES</span></span>

### <span data-ttu-id="433c8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="433c8-108">Example 1</span></span>
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

<span data-ttu-id="433c8-109">Nota: l'impostazione di HealthProbeMethod non è distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="433c8-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="433c8-110">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="433c8-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="433c8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="433c8-111">PARAMETERS</span></span>

### <span data-ttu-id="433c8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433c8-112">-DefaultProfile</span></span>
<span data-ttu-id="433c8-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="433c8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433c8-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="433c8-114">-EnabledState</span></span>
<span data-ttu-id="433c8-115">Se abilitare le sonde di integrità da eseguire con i backend definiti in backendPools.</span><span class="sxs-lookup"><span data-stu-id="433c8-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="433c8-116">Le sonde di integrità possono essere disabilitate solo se è disponibile un singolo backend abilitato in un unico pool di backend abilitato.</span><span class="sxs-lookup"><span data-stu-id="433c8-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="433c8-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="433c8-117">-HealthProbeMethod</span></span>
<span data-ttu-id="433c8-118">Configura il metodo HTTP da usare per sondare i backend definiti in backendPools.</span><span class="sxs-lookup"><span data-stu-id="433c8-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="433c8-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="433c8-119">-IntervalInSeconds</span></span>
<span data-ttu-id="433c8-120">Numero di secondi tra le sonde di integrità.</span><span class="sxs-lookup"><span data-stu-id="433c8-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="433c8-121">Il valore predefinito è 30</span><span class="sxs-lookup"><span data-stu-id="433c8-121">Default value is 30</span></span>

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

### <span data-ttu-id="433c8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="433c8-122">-Name</span></span>
<span data-ttu-id="433c8-123">Nome impostazione sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="433c8-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="433c8-124">-Path</span><span class="sxs-lookup"><span data-stu-id="433c8-124">-Path</span></span>
<span data-ttu-id="433c8-125">Percorso da usare per la sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="433c8-125">The path to use for the health probe.</span></span>
<span data-ttu-id="433c8-126">Il valore predefinito è/</span><span class="sxs-lookup"><span data-stu-id="433c8-126">Default is /</span></span>

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

### <span data-ttu-id="433c8-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="433c8-127">-Protocol</span></span>
<span data-ttu-id="433c8-128">Schema di protocollo da usare per questo valore predefinito di Probe è HTTP</span><span class="sxs-lookup"><span data-stu-id="433c8-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="433c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433c8-129">CommonParameters</span></span>
<span data-ttu-id="433c8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433c8-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="433c8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433c8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="433c8-132">INPUTS</span></span>

### <span data-ttu-id="433c8-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="433c8-133">None</span></span>
## <span data-ttu-id="433c8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="433c8-134">OUTPUTS</span></span>

### <span data-ttu-id="433c8-135">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="433c8-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="433c8-136">Note</span><span class="sxs-lookup"><span data-stu-id="433c8-136">NOTES</span></span>

## <span data-ttu-id="433c8-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="433c8-137">RELATED LINKS</span></span>

<span data-ttu-id="433c8-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="433c8-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
