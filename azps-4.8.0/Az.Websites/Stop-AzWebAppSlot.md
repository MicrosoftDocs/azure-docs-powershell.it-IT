---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: eba40b4c372fd900ac42bead0e2c0b39305c91cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192607"
---
# <span data-ttu-id="a645c-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a645c-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="a645c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a645c-102">SYNOPSIS</span></span>
<span data-ttu-id="a645c-103">Interrompe uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a645c-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="a645c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a645c-104">SYNTAX</span></span>

### <span data-ttu-id="a645c-105">S1</span><span class="sxs-lookup"><span data-stu-id="a645c-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a645c-106">S2</span><span class="sxs-lookup"><span data-stu-id="a645c-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a645c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a645c-107">DESCRIPTION</span></span>
<span data-ttu-id="a645c-108">Il cmdlet **Stop-AzWebAppSlot** arresta uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a645c-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="a645c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a645c-109">EXAMPLES</span></span>

### <span data-ttu-id="a645c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a645c-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a645c-111">Questo comando Arresta lo slot Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="a645c-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a645c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a645c-112">PARAMETERS</span></span>

### <span data-ttu-id="a645c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a645c-113">-DefaultProfile</span></span>
<span data-ttu-id="a645c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a645c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a645c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a645c-115">-Name</span></span>
<span data-ttu-id="a645c-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a645c-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a645c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a645c-117">-ResourceGroupName</span></span>
<span data-ttu-id="a645c-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a645c-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a645c-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a645c-119">-Slot</span></span>
<span data-ttu-id="a645c-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="a645c-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a645c-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="a645c-121">-WebApp</span></span>
<span data-ttu-id="a645c-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a645c-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a645c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a645c-123">CommonParameters</span></span>
<span data-ttu-id="a645c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a645c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a645c-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a645c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a645c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a645c-126">INPUTS</span></span>

### <span data-ttu-id="a645c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a645c-127">System.String</span></span>

### <span data-ttu-id="a645c-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a645c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a645c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a645c-129">OUTPUTS</span></span>

### <span data-ttu-id="a645c-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a645c-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a645c-131">Note</span><span class="sxs-lookup"><span data-stu-id="a645c-131">NOTES</span></span>

## <span data-ttu-id="a645c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a645c-132">RELATED LINKS</span></span>