---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514615"
---
# <span data-ttu-id="de9a1-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="de9a1-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="de9a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="de9a1-102">SYNOPSIS</span></span>
<span data-ttu-id="de9a1-103">Ottiene un profilo di pubblicazione dello slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="de9a1-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de9a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de9a1-104">SYNTAX</span></span>

### <span data-ttu-id="de9a1-105">S1</span><span class="sxs-lookup"><span data-stu-id="de9a1-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de9a1-106">S2</span><span class="sxs-lookup"><span data-stu-id="de9a1-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de9a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de9a1-107">DESCRIPTION</span></span>
<span data-ttu-id="de9a1-108">Il cmdlet **Get-AzureRmWebAppSlotPublishingProfile** ottiene il profilo di pubblicazione dell'app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="de9a1-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="de9a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de9a1-109">EXAMPLES</span></span>

### <span data-ttu-id="de9a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="de9a1-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="de9a1-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="de9a1-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="de9a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="de9a1-112">PARAMETERS</span></span>

### <span data-ttu-id="de9a1-113">-Format</span><span class="sxs-lookup"><span data-stu-id="de9a1-113">-Format</span></span>
<span data-ttu-id="de9a1-114">Formato</span><span class="sxs-lookup"><span data-stu-id="de9a1-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="de9a1-115">-Name</span></span>
<span data-ttu-id="de9a1-116">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="de9a1-116">WebApp Name</span></span>

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

### <span data-ttu-id="de9a1-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="de9a1-117">-OutputFile</span></span>
<span data-ttu-id="de9a1-118">File di output</span><span class="sxs-lookup"><span data-stu-id="de9a1-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de9a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="de9a1-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="de9a1-120">Resource Group Name</span></span>

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

### <span data-ttu-id="de9a1-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="de9a1-121">-Slot</span></span>
<span data-ttu-id="de9a1-122">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="de9a1-122">WebApp Slot Name</span></span>

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

### <span data-ttu-id="de9a1-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="de9a1-123">-WebApp</span></span>
<span data-ttu-id="de9a1-124">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="de9a1-124">WebApp Object</span></span>

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

### <span data-ttu-id="de9a1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9a1-125">-DefaultProfile</span></span>
<span data-ttu-id="de9a1-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de9a1-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de9a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9a1-127">CommonParameters</span></span>
<span data-ttu-id="de9a1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9a1-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de9a1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9a1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="de9a1-130">INPUTS</span></span>

### <span data-ttu-id="de9a1-131">Sito</span><span class="sxs-lookup"><span data-stu-id="de9a1-131">Site</span></span>
<span data-ttu-id="de9a1-132">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="de9a1-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="de9a1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de9a1-133">OUTPUTS</span></span>

## <span data-ttu-id="de9a1-134">Note</span><span class="sxs-lookup"><span data-stu-id="de9a1-134">NOTES</span></span>

## <span data-ttu-id="de9a1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de9a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="de9a1-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="de9a1-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="de9a1-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="de9a1-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="de9a1-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="de9a1-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
