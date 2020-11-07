---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861922"
---
# <span data-ttu-id="85f80-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="85f80-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="85f80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85f80-102">SYNOPSIS</span></span>
<span data-ttu-id="85f80-103">Ottiene gli snapshot disponibili per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="85f80-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="85f80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85f80-104">SYNTAX</span></span>

### <span data-ttu-id="85f80-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="85f80-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="85f80-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="85f80-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="85f80-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85f80-107">DESCRIPTION</span></span>
<span data-ttu-id="85f80-108">Il cmdlet **Get-AzWebAppSnapshot** restituisce tutti gli snapshot per un'app Web.</span><span class="sxs-lookup"><span data-stu-id="85f80-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="85f80-109">Gli snapshot sono backup automatici dei file e delle impostazioni di un'app Web.</span><span class="sxs-lookup"><span data-stu-id="85f80-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="85f80-110">Uno snapshot può essere ripristinato con il cmdlet **Restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="85f80-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="85f80-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85f80-111">EXAMPLES</span></span>

### <span data-ttu-id="85f80-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85f80-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="85f80-113">Ottenere gli snapshot per un'app Web denominata "ConstosoApp" con uno slot denominato "Staging" nel gruppo di risorse "predefinito-Web-Westus"</span><span class="sxs-lookup"><span data-stu-id="85f80-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="85f80-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85f80-114">PARAMETERS</span></span>

### <span data-ttu-id="85f80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f80-115">-DefaultProfile</span></span>
<span data-ttu-id="85f80-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85f80-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f80-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="85f80-117">-Name</span></span>
<span data-ttu-id="85f80-118">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="85f80-118">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f80-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f80-119">-ResourceGroupName</span></span>
<span data-ttu-id="85f80-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85f80-120">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f80-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="85f80-121">-Slot</span></span>
<span data-ttu-id="85f80-122">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="85f80-122">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f80-123">-Web App</span><span class="sxs-lookup"><span data-stu-id="85f80-123">-WebApp</span></span>
<span data-ttu-id="85f80-124">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="85f80-124">The web app object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## <span data-ttu-id="85f80-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85f80-125">INPUTS</span></span>

### <span data-ttu-id="85f80-126">System. String</span><span class="sxs-lookup"><span data-stu-id="85f80-126">System.String</span></span>
<span data-ttu-id="85f80-127">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="85f80-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="85f80-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85f80-128">OUTPUTS</span></span>

### <span data-ttu-id="85f80-129">Microsoft. Azure. Commands. webapps. Cmdlets. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="85f80-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="85f80-130">Note</span><span class="sxs-lookup"><span data-stu-id="85f80-130">NOTES</span></span>

## <span data-ttu-id="85f80-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85f80-131">RELATED LINKS</span></span>

