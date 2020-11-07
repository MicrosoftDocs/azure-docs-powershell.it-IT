---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restart-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restart-AzureRmWebAppSlot.md
ms.openlocfilehash: 08e5f0e1ba87f42f8a2893a63f8f853ece9870c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686987"
---
# <span data-ttu-id="ae28b-101">Restart-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-101">Restart-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="ae28b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae28b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae28b-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae28b-103">SYNTAX</span></span>

### <span data-ttu-id="ae28b-104">S1</span><span class="sxs-lookup"><span data-stu-id="ae28b-104">S1</span></span>
```
Restart-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae28b-105">S2</span><span class="sxs-lookup"><span data-stu-id="ae28b-105">S2</span></span>
```
Restart-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae28b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae28b-106">DESCRIPTION</span></span>
<span data-ttu-id="ae28b-107">Il cmdlet **Restart-AzureRmWebAppSlot** si arresta e quindi avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ae28b-107">The **Restart-AzureRmWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="ae28b-108">Se lo slot per l'app Web si trova in uno stato interrotto, usa il cmdlet Start-AzureRmWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="ae28b-108">If the Web App Slot is in a stopped state, use the Start-AzureRmWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="ae28b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae28b-109">EXAMPLES</span></span>

### <span data-ttu-id="ae28b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae28b-110">Example 1</span></span>
```
PS C:\> Restart-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="ae28b-111">Questo comando Riavvia lo slot Slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="ae28b-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ae28b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae28b-112">PARAMETERS</span></span>

### <span data-ttu-id="ae28b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae28b-113">-DefaultProfile</span></span>
<span data-ttu-id="ae28b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae28b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae28b-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae28b-115">-Name</span></span>
<span data-ttu-id="ae28b-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="ae28b-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae28b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae28b-117">-ResourceGroupName</span></span>
<span data-ttu-id="ae28b-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ae28b-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae28b-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="ae28b-119">-Slot</span></span>
<span data-ttu-id="ae28b-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="ae28b-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae28b-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="ae28b-121">-WebApp</span></span>
<span data-ttu-id="ae28b-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="ae28b-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae28b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae28b-123">CommonParameters</span></span>
<span data-ttu-id="ae28b-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae28b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae28b-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae28b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae28b-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae28b-126">INPUTS</span></span>

### <span data-ttu-id="ae28b-127">Sito</span><span class="sxs-lookup"><span data-stu-id="ae28b-127">Site</span></span>
<span data-ttu-id="ae28b-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ae28b-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ae28b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae28b-129">OUTPUTS</span></span>

## <span data-ttu-id="ae28b-130">Note</span><span class="sxs-lookup"><span data-stu-id="ae28b-130">NOTES</span></span>

## <span data-ttu-id="ae28b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae28b-131">RELATED LINKS</span></span>

[<span data-ttu-id="ae28b-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae28b-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae28b-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae28b-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae28b-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae28b-137">Stop-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ae28b-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="ae28b-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ae28b-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)