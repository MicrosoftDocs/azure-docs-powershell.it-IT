---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861914"
---
# <span data-ttu-id="16ea8-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="16ea8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="16ea8-103">Ottiene uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="16ea8-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="16ea8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16ea8-104">SYNTAX</span></span>

### <span data-ttu-id="16ea8-105">S1</span><span class="sxs-lookup"><span data-stu-id="16ea8-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16ea8-106">S2</span><span class="sxs-lookup"><span data-stu-id="16ea8-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16ea8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ea8-107">DESCRIPTION</span></span>
<span data-ttu-id="16ea8-108">Il cmdlet **Get-AzWebAppSlot** ottiene le informazioni su uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="16ea8-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="16ea8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16ea8-109">EXAMPLES</span></span>

### <span data-ttu-id="16ea8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="16ea8-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="16ea8-111">Questo comando ottiene lo slot denominato Slot001 dall'app Web denominata WebAppStandard che appartiene al gruppo di risorse predefinito-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="16ea8-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="16ea8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16ea8-112">PARAMETERS</span></span>

### <span data-ttu-id="16ea8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ea8-113">-DefaultProfile</span></span>
<span data-ttu-id="16ea8-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16ea8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ea8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="16ea8-115">-Name</span></span>
<span data-ttu-id="16ea8-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="16ea8-116">WebApp Name</span></span>

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

### <span data-ttu-id="16ea8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ea8-117">-ResourceGroupName</span></span>
<span data-ttu-id="16ea8-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="16ea8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="16ea8-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="16ea8-119">-Slot</span></span>
<span data-ttu-id="16ea8-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="16ea8-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ea8-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="16ea8-121">-WebApp</span></span>
<span data-ttu-id="16ea8-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="16ea8-122">WebApp Object</span></span>

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

### <span data-ttu-id="16ea8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ea8-123">CommonParameters</span></span>
<span data-ttu-id="16ea8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ea8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ea8-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ea8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ea8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16ea8-126">INPUTS</span></span>

### <span data-ttu-id="16ea8-127">Sito</span><span class="sxs-lookup"><span data-stu-id="16ea8-127">Site</span></span>
<span data-ttu-id="16ea8-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="16ea8-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="16ea8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16ea8-129">OUTPUTS</span></span>

## <span data-ttu-id="16ea8-130">Note</span><span class="sxs-lookup"><span data-stu-id="16ea8-130">NOTES</span></span>

## <span data-ttu-id="16ea8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16ea8-131">RELATED LINKS</span></span>

[<span data-ttu-id="16ea8-132">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="16ea8-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="16ea8-134">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="16ea8-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="16ea8-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="16ea8-137">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16ea8-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="16ea8-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="16ea8-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
