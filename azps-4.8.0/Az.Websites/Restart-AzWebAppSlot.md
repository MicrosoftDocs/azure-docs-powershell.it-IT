---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 377e08f344256f6d744fec66f0b6b20f495d9309
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032758"
---
# <span data-ttu-id="4d3f5-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="4d3f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d3f5-102">SYNOPSIS</span></span>

## <span data-ttu-id="4d3f5-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d3f5-103">SYNTAX</span></span>

### <span data-ttu-id="4d3f5-104">S1</span><span class="sxs-lookup"><span data-stu-id="4d3f5-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d3f5-105">S2</span><span class="sxs-lookup"><span data-stu-id="4d3f5-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d3f5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d3f5-106">DESCRIPTION</span></span>
<span data-ttu-id="4d3f5-107">Il cmdlet **Restart-AzWebAppSlot** si arresta e quindi avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="4d3f5-108">Se lo slot per l'app Web si trova in uno stato interrotto, usa il cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="4d3f5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d3f5-109">EXAMPLES</span></span>

### <span data-ttu-id="4d3f5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d3f5-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="4d3f5-111">Questo comando Riavvia lo slot Slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="4d3f5-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4d3f5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d3f5-112">PARAMETERS</span></span>

### <span data-ttu-id="4d3f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3f5-113">-DefaultProfile</span></span>
<span data-ttu-id="4d3f5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d3f5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d3f5-115">-Name</span></span>
<span data-ttu-id="4d3f5-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="4d3f5-116">WebApp Name</span></span>

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

### <span data-ttu-id="4d3f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d3f5-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4d3f5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4d3f5-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-119">-Slot</span></span>
<span data-ttu-id="4d3f5-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="4d3f5-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="4d3f5-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="4d3f5-121">-WebApp</span></span>
<span data-ttu-id="4d3f5-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="4d3f5-122">WebApp Object</span></span>

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

### <span data-ttu-id="4d3f5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3f5-123">CommonParameters</span></span>
<span data-ttu-id="4d3f5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3f5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3f5-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d3f5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3f5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d3f5-126">INPUTS</span></span>

### <span data-ttu-id="4d3f5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4d3f5-127">System.String</span></span>

### <span data-ttu-id="4d3f5-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4d3f5-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d3f5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d3f5-129">OUTPUTS</span></span>

### <span data-ttu-id="4d3f5-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4d3f5-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="4d3f5-131">Note</span><span class="sxs-lookup"><span data-stu-id="4d3f5-131">NOTES</span></span>

## <span data-ttu-id="4d3f5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d3f5-132">RELATED LINKS</span></span>

[<span data-ttu-id="4d3f5-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="4d3f5-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="4d3f5-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="4d3f5-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="4d3f5-137">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="4d3f5-138">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="4d3f5-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="4d3f5-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4d3f5-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
