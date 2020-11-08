---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192612"
---
# <span data-ttu-id="6cea0-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="6cea0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cea0-102">SYNOPSIS</span></span>
<span data-ttu-id="6cea0-103">Ottiene uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6cea0-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="6cea0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cea0-104">SYNTAX</span></span>

### <span data-ttu-id="6cea0-105">S1</span><span class="sxs-lookup"><span data-stu-id="6cea0-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6cea0-106">S2</span><span class="sxs-lookup"><span data-stu-id="6cea0-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cea0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cea0-107">DESCRIPTION</span></span>
<span data-ttu-id="6cea0-108">Il cmdlet **Get-AzWebAppSlot** ottiene le informazioni su uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="6cea0-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="6cea0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cea0-109">EXAMPLES</span></span>

### <span data-ttu-id="6cea0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6cea0-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="6cea0-111">Questo comando ottiene lo slot denominato Slot001 dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="6cea0-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6cea0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cea0-112">PARAMETERS</span></span>

### <span data-ttu-id="6cea0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cea0-113">-DefaultProfile</span></span>
<span data-ttu-id="6cea0-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6cea0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cea0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cea0-115">-Name</span></span>
<span data-ttu-id="6cea0-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="6cea0-116">WebApp Name</span></span>

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

### <span data-ttu-id="6cea0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cea0-117">-ResourceGroupName</span></span>
<span data-ttu-id="6cea0-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="6cea0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="6cea0-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="6cea0-119">-Slot</span></span>
<span data-ttu-id="6cea0-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="6cea0-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cea0-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="6cea0-121">-WebApp</span></span>
<span data-ttu-id="6cea0-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="6cea0-122">WebApp Object</span></span>

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

### <span data-ttu-id="6cea0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cea0-123">CommonParameters</span></span>
<span data-ttu-id="6cea0-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cea0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cea0-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cea0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cea0-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cea0-126">INPUTS</span></span>

### <span data-ttu-id="6cea0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6cea0-127">System.String</span></span>

### <span data-ttu-id="6cea0-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6cea0-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6cea0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cea0-129">OUTPUTS</span></span>

### <span data-ttu-id="6cea0-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="6cea0-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6cea0-131">Note</span><span class="sxs-lookup"><span data-stu-id="6cea0-131">NOTES</span></span>

## <span data-ttu-id="6cea0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cea0-132">RELATED LINKS</span></span>

[<span data-ttu-id="6cea0-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="6cea0-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="6cea0-135">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="6cea0-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="6cea0-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="6cea0-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="6cea0-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="6cea0-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="6cea0-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
