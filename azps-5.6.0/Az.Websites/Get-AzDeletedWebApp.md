---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: a67e48cdcad9d80d244e74ef8e20f81fcbd157cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983886"
---
# <span data-ttu-id="f21d1-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f21d1-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="f21d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f21d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f21d1-103">Vengono eliminate app Web nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f21d1-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="f21d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f21d1-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f21d1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f21d1-105">DESCRIPTION</span></span>
<span data-ttu-id="f21d1-106">Il **cmdlet Get-AzDeletedWebApp restituisce** tutte le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="f21d1-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="f21d1-107">Facoltativamente, le app eliminate possono essere filtrate per gruppo di risorse, nome e slot.</span><span class="sxs-lookup"><span data-stu-id="f21d1-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="f21d1-108">Possono essere presenti più app eliminate con lo stesso nome e gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f21d1-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="f21d1-109">Selezionare DeletionTime per distinguere le app eliminate che condividono lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="f21d1-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="f21d1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f21d1-110">EXAMPLES</span></span>

### <span data-ttu-id="f21d1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f21d1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f21d1-112">Questo comando recupera le app eliminate denominate ContosoSite appartenenti al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="f21d1-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f21d1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f21d1-113">PARAMETERS</span></span>

### <span data-ttu-id="f21d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f21d1-114">-DefaultProfile</span></span>
<span data-ttu-id="f21d1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f21d1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f21d1-116">-Location</span><span class="sxs-lookup"><span data-stu-id="f21d1-116">-Location</span></span>
<span data-ttu-id="f21d1-117">Posizione dell'app eliminata.</span><span class="sxs-lookup"><span data-stu-id="f21d1-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21d1-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f21d1-118">-Name</span></span>
<span data-ttu-id="f21d1-119">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="f21d1-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f21d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="f21d1-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f21d1-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f21d1-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="f21d1-122">-Slot</span></span>
<span data-ttu-id="f21d1-123">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="f21d1-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f21d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f21d1-124">CommonParameters</span></span>
<span data-ttu-id="f21d1-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f21d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f21d1-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f21d1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f21d1-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="f21d1-127">INPUTS</span></span>

### <span data-ttu-id="f21d1-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f21d1-128">None</span></span>

## <span data-ttu-id="f21d1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f21d1-129">OUTPUTS</span></span>

### <span data-ttu-id="f21d1-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f21d1-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="f21d1-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="f21d1-131">NOTES</span></span>

## <span data-ttu-id="f21d1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f21d1-132">RELATED LINKS</span></span>

[<span data-ttu-id="f21d1-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="f21d1-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)