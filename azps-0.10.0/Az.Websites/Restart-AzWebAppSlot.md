---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 645E74D2-640D-494F-9798-4375FE6A0AF2
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restart-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restart-AzWebAppSlot.md
ms.openlocfilehash: 9f0e48b20d19113290784d65b6bc78531dc7b2a1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861838"
---
# <span data-ttu-id="59cf5-101">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-101">Restart-AzWebAppSlot</span></span>

## <span data-ttu-id="59cf5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59cf5-102">SYNOPSIS</span></span>

## <span data-ttu-id="59cf5-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59cf5-103">SYNTAX</span></span>

### <span data-ttu-id="59cf5-104">S1</span><span class="sxs-lookup"><span data-stu-id="59cf5-104">S1</span></span>
```
Restart-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59cf5-105">S2</span><span class="sxs-lookup"><span data-stu-id="59cf5-105">S2</span></span>
```
Restart-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59cf5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59cf5-106">DESCRIPTION</span></span>
<span data-ttu-id="59cf5-107">Il cmdlet **Restart-AzWebAppSlot** si arresta e quindi avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="59cf5-107">The **Restart-AzWebAppSlot** cmdlet stops and then starts an Azure Web App Slot.</span></span>
<span data-ttu-id="59cf5-108">Se lo slot per l'app Web si trova in uno stato interrotto, usa il cmdlet Start-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="59cf5-108">If the Web App Slot is in a stopped state, use the Start-AzWebAppSlot cmdlet.</span></span>

## <span data-ttu-id="59cf5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59cf5-109">EXAMPLES</span></span>

### <span data-ttu-id="59cf5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59cf5-110">Example 1</span></span>
```
PS C:\> Restart-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="59cf5-111">Questo comando Riavvia lo slot Slot001 per l'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus</span><span class="sxs-lookup"><span data-stu-id="59cf5-111">This command restarts the slot Slot001 for the web app ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="59cf5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59cf5-112">PARAMETERS</span></span>

### <span data-ttu-id="59cf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59cf5-113">-DefaultProfile</span></span>
<span data-ttu-id="59cf5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59cf5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59cf5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="59cf5-115">-Name</span></span>
<span data-ttu-id="59cf5-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="59cf5-116">WebApp Name</span></span>

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

### <span data-ttu-id="59cf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59cf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="59cf5-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="59cf5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="59cf5-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="59cf5-119">-Slot</span></span>
<span data-ttu-id="59cf5-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="59cf5-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="59cf5-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="59cf5-121">-WebApp</span></span>
<span data-ttu-id="59cf5-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="59cf5-122">WebApp Object</span></span>

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

### <span data-ttu-id="59cf5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59cf5-123">CommonParameters</span></span>
<span data-ttu-id="59cf5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59cf5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59cf5-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59cf5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59cf5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59cf5-126">INPUTS</span></span>

### <span data-ttu-id="59cf5-127">Sito</span><span class="sxs-lookup"><span data-stu-id="59cf5-127">Site</span></span>
<span data-ttu-id="59cf5-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="59cf5-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="59cf5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59cf5-129">OUTPUTS</span></span>

## <span data-ttu-id="59cf5-130">Note</span><span class="sxs-lookup"><span data-stu-id="59cf5-130">NOTES</span></span>

## <span data-ttu-id="59cf5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59cf5-131">RELATED LINKS</span></span>

[<span data-ttu-id="59cf5-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="59cf5-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="59cf5-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="59cf5-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="59cf5-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="59cf5-137">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59cf5-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="59cf5-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="59cf5-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
