---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515332"
---
# <span data-ttu-id="849a9-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="849a9-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="849a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="849a9-102">SYNOPSIS</span></span>
<span data-ttu-id="849a9-103">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="849a9-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="849a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="849a9-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="849a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="849a9-105">DESCRIPTION</span></span>
<span data-ttu-id="849a9-106">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="849a9-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="849a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="849a9-107">EXAMPLES</span></span>

### <span data-ttu-id="849a9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="849a9-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="849a9-109">Creare un oggetto PSHealthProbeSetting per la creazione di porte anteriori</span><span class="sxs-lookup"><span data-stu-id="849a9-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="849a9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="849a9-110">PARAMETERS</span></span>

### <span data-ttu-id="849a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849a9-111">-DefaultProfile</span></span>
<span data-ttu-id="849a9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="849a9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849a9-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="849a9-113">-IntervalInSeconds</span></span>
<span data-ttu-id="849a9-114">Numero di secondi tra le sonde di integrità.</span><span class="sxs-lookup"><span data-stu-id="849a9-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="849a9-115">Il valore predefinito è 30</span><span class="sxs-lookup"><span data-stu-id="849a9-115">Default value is 30</span></span>

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

### <span data-ttu-id="849a9-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="849a9-116">-Name</span></span>
<span data-ttu-id="849a9-117">Nome impostazione sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="849a9-117">health probe setting name.</span></span>

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

### <span data-ttu-id="849a9-118">-Path</span><span class="sxs-lookup"><span data-stu-id="849a9-118">-Path</span></span>
<span data-ttu-id="849a9-119">Percorso da usare per la sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="849a9-119">The path to use for the health probe.</span></span>
<span data-ttu-id="849a9-120">Il valore predefinito è/</span><span class="sxs-lookup"><span data-stu-id="849a9-120">Default is /</span></span>

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

### <span data-ttu-id="849a9-121">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="849a9-121">-Protocol</span></span>
<span data-ttu-id="849a9-122">Schema di protocollo da usare per questo valore predefinito di Probe è HTTP</span><span class="sxs-lookup"><span data-stu-id="849a9-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="849a9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849a9-123">CommonParameters</span></span>
<span data-ttu-id="849a9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849a9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849a9-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="849a9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849a9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="849a9-126">INPUTS</span></span>

### <span data-ttu-id="849a9-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="849a9-127">None</span></span>

## <span data-ttu-id="849a9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="849a9-128">OUTPUTS</span></span>

### <span data-ttu-id="849a9-129">Microsoft. Azure. Commands. FrontDoor. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="849a9-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="849a9-130">Note</span><span class="sxs-lookup"><span data-stu-id="849a9-130">NOTES</span></span>

## <span data-ttu-id="849a9-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="849a9-131">RELATED LINKS</span></span>

<span data-ttu-id="849a9-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="849a9-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
