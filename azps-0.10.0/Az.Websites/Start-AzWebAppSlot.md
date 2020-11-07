---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861826"
---
# <span data-ttu-id="bcaff-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="bcaff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcaff-102">SYNOPSIS</span></span>
<span data-ttu-id="bcaff-103">Avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bcaff-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="bcaff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcaff-104">SYNTAX</span></span>

### <span data-ttu-id="bcaff-105">S1</span><span class="sxs-lookup"><span data-stu-id="bcaff-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcaff-106">S2</span><span class="sxs-lookup"><span data-stu-id="bcaff-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcaff-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcaff-107">DESCRIPTION</span></span>
<span data-ttu-id="bcaff-108">Il cmdlet **Start-AzWebAppSlot** avvia uno slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bcaff-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="bcaff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcaff-109">EXAMPLES</span></span>

### <span data-ttu-id="bcaff-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bcaff-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="bcaff-111">Questo comando avvia lo slot denominato Slot001 pertinente all'app Web denominata ContosoWebApp che appartiene al gruppo di risorse denominato Default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="bcaff-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bcaff-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcaff-112">PARAMETERS</span></span>

### <span data-ttu-id="bcaff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcaff-113">-DefaultProfile</span></span>
<span data-ttu-id="bcaff-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcaff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcaff-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcaff-115">-Name</span></span>
<span data-ttu-id="bcaff-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="bcaff-116">WebApp Name</span></span>

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

### <span data-ttu-id="bcaff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcaff-117">-ResourceGroupName</span></span>
<span data-ttu-id="bcaff-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="bcaff-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bcaff-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="bcaff-119">-Slot</span></span>
<span data-ttu-id="bcaff-120">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="bcaff-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="bcaff-121">-Web App</span><span class="sxs-lookup"><span data-stu-id="bcaff-121">-WebApp</span></span>
<span data-ttu-id="bcaff-122">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="bcaff-122">WebApp Object</span></span>

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

### <span data-ttu-id="bcaff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcaff-123">CommonParameters</span></span>
<span data-ttu-id="bcaff-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcaff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcaff-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcaff-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcaff-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcaff-126">INPUTS</span></span>

### <span data-ttu-id="bcaff-127">Sito</span><span class="sxs-lookup"><span data-stu-id="bcaff-127">Site</span></span>
<span data-ttu-id="bcaff-128">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bcaff-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bcaff-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcaff-129">OUTPUTS</span></span>

## <span data-ttu-id="bcaff-130">Note</span><span class="sxs-lookup"><span data-stu-id="bcaff-130">NOTES</span></span>

## <span data-ttu-id="bcaff-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcaff-131">RELATED LINKS</span></span>

[<span data-ttu-id="bcaff-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="bcaff-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="bcaff-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="bcaff-135">Riavviare-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="bcaff-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="bcaff-137">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="bcaff-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="bcaff-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bcaff-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
