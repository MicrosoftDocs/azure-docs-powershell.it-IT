---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: ace1b16bc6d89fb619daba23a214326acd8d0d24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508487"
---
# <span data-ttu-id="cc1a1-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="cc1a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc1a1-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc1a1-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc1a1-103">SYNTAX</span></span>

### <span data-ttu-id="cc1a1-104">S1</span><span class="sxs-lookup"><span data-stu-id="cc1a1-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc1a1-105">S2</span><span class="sxs-lookup"><span data-stu-id="cc1a1-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc1a1-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc1a1-106">DESCRIPTION</span></span>
<span data-ttu-id="cc1a1-107">Il cmdlet **Restart-AzureRmWebAppSlot** si arresta e quindi avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="cc1a1-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="cc1a1-108">Se lo slot per l'app Web si trova in uno stato interrotto, usa il cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cc1a1-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="cc1a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc1a1-109">EXAMPLES</span></span>

### <span data-ttu-id="cc1a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cc1a1-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="cc1a1-111">Questo comando Riavvia lo slot Slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="cc1a1-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="cc1a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc1a1-112">PARAMETERS</span></span>

### <span data-ttu-id="cc1a1-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cc1a1-113">-Name</span></span>
<span data-ttu-id="cc1a1-114">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="cc1a1-114">WebApp Name</span></span>

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

### <span data-ttu-id="cc1a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="cc1a1-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cc1a1-116">Resource Group Name</span></span>

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

### <span data-ttu-id="cc1a1-117">-Slot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-117">-Slot</span></span>
<span data-ttu-id="cc1a1-118">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="cc1a1-118">WebApp Slot Name</span></span>

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

### <span data-ttu-id="cc1a1-119">-Web App</span><span class="sxs-lookup"><span data-stu-id="cc1a1-119">-WebApp</span></span>
<span data-ttu-id="cc1a1-120">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="cc1a1-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc1a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1a1-121">-DefaultProfile</span></span>
<span data-ttu-id="cc1a1-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc1a1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc1a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1a1-123">CommonParameters</span></span>
<span data-ttu-id="cc1a1-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1a1-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc1a1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1a1-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc1a1-126">INPUTS</span></span>

### <span data-ttu-id="cc1a1-127">Sito</span><span class="sxs-lookup"><span data-stu-id="cc1a1-127">Site</span></span>
<span data-ttu-id="cc1a1-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cc1a1-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="cc1a1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc1a1-129">OUTPUTS</span></span>

## <span data-ttu-id="cc1a1-130">Note</span><span class="sxs-lookup"><span data-stu-id="cc1a1-130">NOTES</span></span>

## <span data-ttu-id="cc1a1-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc1a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="cc1a1-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="cc1a1-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="cc1a1-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="cc1a1-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="cc1a1-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="cc1a1-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cc1a1-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="cc1a1-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="cc1a1-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
