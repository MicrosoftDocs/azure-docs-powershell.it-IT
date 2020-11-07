---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674381"
---
# <span data-ttu-id="49429-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="49429-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="49429-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49429-102">SYNOPSIS</span></span>
<span data-ttu-id="49429-103">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="49429-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="49429-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49429-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49429-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49429-105">DESCRIPTION</span></span>
<span data-ttu-id="49429-106">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="49429-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="49429-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49429-107">EXAMPLES</span></span>

### <span data-ttu-id="49429-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49429-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="49429-109">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="49429-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="49429-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49429-110">PARAMETERS</span></span>

### <span data-ttu-id="49429-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49429-111">-DefaultProfile</span></span>
<span data-ttu-id="49429-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49429-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49429-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="49429-113">-IntervalInSeconds</span></span>
<span data-ttu-id="49429-114">Numero di secondi tra le sonde di integrità.</span><span class="sxs-lookup"><span data-stu-id="49429-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="49429-115">Il valore predefinito è 30</span><span class="sxs-lookup"><span data-stu-id="49429-115">Default value is 30</span></span>

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

### <span data-ttu-id="49429-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="49429-116">-Name</span></span>
<span data-ttu-id="49429-117">Nome impostazione sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="49429-117">health probe setting name.</span></span>

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

### <span data-ttu-id="49429-118">-Path</span><span class="sxs-lookup"><span data-stu-id="49429-118">-Path</span></span>
<span data-ttu-id="49429-119">Percorso da usare per la sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="49429-119">The path to use for the health probe.</span></span>
<span data-ttu-id="49429-120">Il valore predefinito è/</span><span class="sxs-lookup"><span data-stu-id="49429-120">Default is /</span></span>

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

### <span data-ttu-id="49429-121">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="49429-121">-Protocol</span></span>
<span data-ttu-id="49429-122">Schema di protocollo da usare per questo valore predefinito di Probe è HTTP</span><span class="sxs-lookup"><span data-stu-id="49429-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="49429-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49429-123">CommonParameters</span></span>
<span data-ttu-id="49429-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49429-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49429-125">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49429-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49429-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49429-126">INPUTS</span></span>

### <span data-ttu-id="49429-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="49429-127">None</span></span>

## <span data-ttu-id="49429-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49429-128">OUTPUTS</span></span>

### <span data-ttu-id="49429-129">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="49429-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="49429-130">Note</span><span class="sxs-lookup"><span data-stu-id="49429-130">NOTES</span></span>

## <span data-ttu-id="49429-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49429-131">RELATED LINKS</span></span>

<span data-ttu-id="49429-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="49429-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
