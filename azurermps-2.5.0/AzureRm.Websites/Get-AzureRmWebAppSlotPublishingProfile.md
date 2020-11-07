---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 17ad6612ff36539d212c20c2321c6292fb63a499
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866622"
---
# <span data-ttu-id="31b7a-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="31b7a-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="31b7a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31b7a-102">SYNOPSIS</span></span>
<span data-ttu-id="31b7a-103">Ottiene un profilo di pubblicazione dello slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="31b7a-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b7a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b7a-104">SYNTAX</span></span>

### <span data-ttu-id="31b7a-105">S1</span><span class="sxs-lookup"><span data-stu-id="31b7a-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31b7a-106">S2</span><span class="sxs-lookup"><span data-stu-id="31b7a-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b7a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b7a-107">DESCRIPTION</span></span>
<span data-ttu-id="31b7a-108">Il cmdlet **Get-AzureRmWebAppSlotPublishingProfile** ottiene il profilo di pubblicazione dell'app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="31b7a-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="31b7a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b7a-109">EXAMPLES</span></span>

### <span data-ttu-id="31b7a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31b7a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="31b7a-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="31b7a-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="31b7a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31b7a-112">PARAMETERS</span></span>

### <span data-ttu-id="31b7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b7a-113">-DefaultProfile</span></span>
<span data-ttu-id="31b7a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31b7a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b7a-115">-Format</span><span class="sxs-lookup"><span data-stu-id="31b7a-115">-Format</span></span>
<span data-ttu-id="31b7a-116">Formato</span><span class="sxs-lookup"><span data-stu-id="31b7a-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b7a-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31b7a-117">-Name</span></span>
<span data-ttu-id="31b7a-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="31b7a-118">WebApp Name</span></span>

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

### <span data-ttu-id="31b7a-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="31b7a-119">-OutputFile</span></span>
<span data-ttu-id="31b7a-120">File di output</span><span class="sxs-lookup"><span data-stu-id="31b7a-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31b7a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31b7a-121">-ResourceGroupName</span></span>
<span data-ttu-id="31b7a-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="31b7a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="31b7a-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="31b7a-123">-Slot</span></span>
<span data-ttu-id="31b7a-124">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="31b7a-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="31b7a-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="31b7a-125">-WebApp</span></span>
<span data-ttu-id="31b7a-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="31b7a-126">WebApp Object</span></span>

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

### <span data-ttu-id="31b7a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b7a-127">CommonParameters</span></span>
<span data-ttu-id="31b7a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b7a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b7a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b7a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b7a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31b7a-130">INPUTS</span></span>

### <span data-ttu-id="31b7a-131">Sito</span><span class="sxs-lookup"><span data-stu-id="31b7a-131">Site</span></span>
<span data-ttu-id="31b7a-132">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="31b7a-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="31b7a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b7a-133">OUTPUTS</span></span>

## <span data-ttu-id="31b7a-134">Note</span><span class="sxs-lookup"><span data-stu-id="31b7a-134">NOTES</span></span>

## <span data-ttu-id="31b7a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b7a-135">RELATED LINKS</span></span>

[<span data-ttu-id="31b7a-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="31b7a-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="31b7a-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="31b7a-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="31b7a-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="31b7a-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
