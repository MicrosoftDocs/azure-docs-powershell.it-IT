---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: a89ebd3142d738664cd80cab198bd6f791c1287a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676311"
---
# <span data-ttu-id="f6624-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f6624-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f6624-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6624-102">SYNOPSIS</span></span>
<span data-ttu-id="f6624-103">Ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f6624-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f6624-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6624-104">SYNTAX</span></span>

### <span data-ttu-id="f6624-105">S1</span><span class="sxs-lookup"><span data-stu-id="f6624-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6624-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6624-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6624-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6624-107">DESCRIPTION</span></span>
<span data-ttu-id="f6624-108">Il cmdlet **Get-AzWebAppPublishingProfile** ottiene un profilo di pubblicazione di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f6624-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f6624-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6624-109">EXAMPLES</span></span>

### <span data-ttu-id="f6624-110">1:</span><span class="sxs-lookup"><span data-stu-id="f6624-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="f6624-111">Questo comando consente di ottenere il profilo di pubblicazione in formato FTP per l'app Web ContosoWebApp associato al gruppo di risorse predefinito-Web-Westus e lo archivia nel file di output specificato.</span><span class="sxs-lookup"><span data-stu-id="f6624-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="f6624-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6624-112">PARAMETERS</span></span>

### <span data-ttu-id="f6624-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6624-113">-DefaultProfile</span></span>
<span data-ttu-id="f6624-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6624-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6624-115">-Format</span><span class="sxs-lookup"><span data-stu-id="f6624-115">-Format</span></span>
<span data-ttu-id="f6624-116">Formato</span><span class="sxs-lookup"><span data-stu-id="f6624-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6624-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="f6624-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="f6624-118">Includere gli endpoint di ripristino di emergenza se vero</span><span class="sxs-lookup"><span data-stu-id="f6624-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6624-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6624-119">-Name</span></span>
<span data-ttu-id="f6624-120">Nome Web App</span><span class="sxs-lookup"><span data-stu-id="f6624-120">WebApp Name</span></span>

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

### <span data-ttu-id="f6624-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f6624-121">-OutputFile</span></span>
<span data-ttu-id="f6624-122">File di output</span><span class="sxs-lookup"><span data-stu-id="f6624-122">Output File</span></span>

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

### <span data-ttu-id="f6624-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6624-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6624-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="f6624-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f6624-125">-Web App</span><span class="sxs-lookup"><span data-stu-id="f6624-125">-WebApp</span></span>
<span data-ttu-id="f6624-126">Oggetto Web App</span><span class="sxs-lookup"><span data-stu-id="f6624-126">WebApp Object</span></span>

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

### <span data-ttu-id="f6624-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6624-127">CommonParameters</span></span>
<span data-ttu-id="f6624-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6624-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6624-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6624-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6624-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6624-130">INPUTS</span></span>

### <span data-ttu-id="f6624-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f6624-131">System.String</span></span>

### <span data-ttu-id="f6624-132">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f6624-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6624-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6624-133">OUTPUTS</span></span>

### <span data-ttu-id="f6624-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f6624-134">System.String</span></span>

## <span data-ttu-id="f6624-135">Note</span><span class="sxs-lookup"><span data-stu-id="f6624-135">NOTES</span></span>

## <span data-ttu-id="f6624-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6624-136">RELATED LINKS</span></span>

[<span data-ttu-id="f6624-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f6624-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f6624-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f6624-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

