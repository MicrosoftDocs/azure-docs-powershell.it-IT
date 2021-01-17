---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476316"
---
# <span data-ttu-id="1931f-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="1931f-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="1931f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1931f-102">SYNOPSIS</span></span>
<span data-ttu-id="1931f-103">Crea un oggetto PSBackendPoolsSetting per la creazione di porte anteriori.</span><span class="sxs-lookup"><span data-stu-id="1931f-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="1931f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1931f-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1931f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1931f-105">DESCRIPTION</span></span>
<span data-ttu-id="1931f-106">Il cmdlet **New-AzFrontDoorBackendpoolsSettingObject** crea un nuovo oggetto PSBackendPoolsSettings per la creazione di porte anteriori.</span><span class="sxs-lookup"><span data-stu-id="1931f-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="1931f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1931f-107">EXAMPLES</span></span>

### <span data-ttu-id="1931f-108">Esempio 1: creare un oggetto BackendPoolsSettings usando le impostazioni predefinite</span><span class="sxs-lookup"><span data-stu-id="1931f-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="1931f-109">Esempio 2: creare un oggetto BackendPoolsSettings con valori specificati dall'utente</span><span class="sxs-lookup"><span data-stu-id="1931f-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="1931f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1931f-110">PARAMETERS</span></span>

### <span data-ttu-id="1931f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1931f-111">-DefaultProfile</span></span>
<span data-ttu-id="1931f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1931f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1931f-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="1931f-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="1931f-114">Se applicare il controllo nome certificato alle richieste HTTPS a tutti i pool back-end.</span><span class="sxs-lookup"><span data-stu-id="1931f-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="1931f-115">Nessun effetto sulle richieste non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1931f-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="1931f-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1931f-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="1931f-117">Timeout di invio e ricezione su richiesta di inoltro al backend.</span><span class="sxs-lookup"><span data-stu-id="1931f-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="1931f-118">Quando viene raggiunto il timeout, la richiesta non riesce e viene restituita.</span><span class="sxs-lookup"><span data-stu-id="1931f-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="1931f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1931f-119">CommonParameters</span></span>
<span data-ttu-id="1931f-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1931f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1931f-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1931f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1931f-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1931f-122">INPUTS</span></span>

### <span data-ttu-id="1931f-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1931f-123">None</span></span>

## <span data-ttu-id="1931f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1931f-124">OUTPUTS</span></span>

### <span data-ttu-id="1931f-125">Microsoft. Azure. Commands. FrontDoor. Models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="1931f-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="1931f-126">Note</span><span class="sxs-lookup"><span data-stu-id="1931f-126">NOTES</span></span>

## <span data-ttu-id="1931f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1931f-127">RELATED LINKS</span></span>
