---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: cedaf16333d69a25dce0ce2657640e723767aece
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861910"
---
# <span data-ttu-id="e10a1-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e10a1-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e10a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e10a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e10a1-103">Ottiene un profilo di pubblicazione dello slot di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e10a1-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="e10a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e10a1-104">SYNTAX</span></span>

### <span data-ttu-id="e10a1-105">S1</span><span class="sxs-lookup"><span data-stu-id="e10a1-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e10a1-106">S2</span><span class="sxs-lookup"><span data-stu-id="e10a1-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e10a1-107">DESCRIPTION</span></span>
<span data-ttu-id="e10a1-108">Il cmdlet **Get-AzWebAppSlotPublishingProfile** ottiene il profilo di pubblicazione dell'app Web per lo slot specificato.</span><span class="sxs-lookup"><span data-stu-id="e10a1-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="e10a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e10a1-109">EXAMPLES</span></span>

### <span data-ttu-id="e10a1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e10a1-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="e10a1-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per gli slot Slot001 relativi all'app Web ContosoWebApp associata al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="e10a1-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="e10a1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e10a1-112">PARAMETERS</span></span>

### <span data-ttu-id="e10a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10a1-113">-DefaultProfile</span></span>
<span data-ttu-id="e10a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e10a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e10a1-115">-Format</span><span class="sxs-lookup"><span data-stu-id="e10a1-115">-Format</span></span>
<span data-ttu-id="e10a1-116">Formato</span><span class="sxs-lookup"><span data-stu-id="e10a1-116">Format</span></span>

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

### <span data-ttu-id="e10a1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e10a1-117">-Name</span></span>
<span data-ttu-id="e10a1-118">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="e10a1-118">WebApp Name</span></span>

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

### <span data-ttu-id="e10a1-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="e10a1-119">-OutputFile</span></span>
<span data-ttu-id="e10a1-120">File di output</span><span class="sxs-lookup"><span data-stu-id="e10a1-120">Output File</span></span>

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

### <span data-ttu-id="e10a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="e10a1-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="e10a1-122">Resource Group Name</span></span>

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

### <span data-ttu-id="e10a1-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="e10a1-123">-Slot</span></span>
<span data-ttu-id="e10a1-124">Nome dello slot Web App</span><span class="sxs-lookup"><span data-stu-id="e10a1-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="e10a1-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="e10a1-125">-WebApp</span></span>
<span data-ttu-id="e10a1-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="e10a1-126">WebApp Object</span></span>

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

### <span data-ttu-id="e10a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10a1-127">CommonParameters</span></span>
<span data-ttu-id="e10a1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10a1-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e10a1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10a1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e10a1-130">INPUTS</span></span>

### <span data-ttu-id="e10a1-131">Sito</span><span class="sxs-lookup"><span data-stu-id="e10a1-131">Site</span></span>
<span data-ttu-id="e10a1-132">Il parametro "Web App" accetta il valore di tipo "sito" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e10a1-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e10a1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e10a1-133">OUTPUTS</span></span>

## <span data-ttu-id="e10a1-134">Note</span><span class="sxs-lookup"><span data-stu-id="e10a1-134">NOTES</span></span>

## <span data-ttu-id="e10a1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e10a1-135">RELATED LINKS</span></span>

[<span data-ttu-id="e10a1-136">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e10a1-136">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="e10a1-137">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="e10a1-137">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="e10a1-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e10a1-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
