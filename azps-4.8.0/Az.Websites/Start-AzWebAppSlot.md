---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192611"
---
# <span data-ttu-id="a1b43-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="a1b43-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1b43-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b43-103">Avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a1b43-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="a1b43-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1b43-104">SYNTAX</span></span>

### <span data-ttu-id="a1b43-105">S1</span><span class="sxs-lookup"><span data-stu-id="a1b43-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1b43-106">S2</span><span class="sxs-lookup"><span data-stu-id="a1b43-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1b43-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1b43-107">DESCRIPTION</span></span>
<span data-ttu-id="a1b43-108">Il cmdlet **Start-AzWebAppSlot** avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a1b43-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="a1b43-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1b43-109">EXAMPLES</span></span>

### <span data-ttu-id="a1b43-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1b43-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="a1b43-111">Questo comando avvia lo slot denominato Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="a1b43-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1b43-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1b43-112">PARAMETERS</span></span>

### <span data-ttu-id="a1b43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b43-113">-DefaultProfile</span></span>
<span data-ttu-id="a1b43-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b43-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1b43-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b43-115">-Name</span></span>
<span data-ttu-id="a1b43-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="a1b43-116">WebApp Name</span></span>

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

### <span data-ttu-id="a1b43-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b43-117">-ResourceGroupName</span></span>
<span data-ttu-id="a1b43-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a1b43-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a1b43-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="a1b43-119">-Slot</span></span>
<span data-ttu-id="a1b43-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="a1b43-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a1b43-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="a1b43-121">-WebApp</span></span>
<span data-ttu-id="a1b43-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="a1b43-122">WebApp Object</span></span>

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

### <span data-ttu-id="a1b43-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b43-123">CommonParameters</span></span>
<span data-ttu-id="a1b43-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b43-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b43-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b43-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b43-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1b43-126">INPUTS</span></span>

### <span data-ttu-id="a1b43-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b43-127">System.String</span></span>

### <span data-ttu-id="a1b43-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a1b43-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a1b43-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1b43-129">OUTPUTS</span></span>

### <span data-ttu-id="a1b43-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="a1b43-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a1b43-131">Note</span><span class="sxs-lookup"><span data-stu-id="a1b43-131">NOTES</span></span>

## <span data-ttu-id="a1b43-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1b43-132">RELATED LINKS</span></span>

[<span data-ttu-id="a1b43-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="a1b43-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="a1b43-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="a1b43-136">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="a1b43-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="a1b43-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a1b43-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="a1b43-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1b43-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
