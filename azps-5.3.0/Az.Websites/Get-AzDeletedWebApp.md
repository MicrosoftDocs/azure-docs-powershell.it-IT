---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474788"
---
# <span data-ttu-id="5053d-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5053d-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="5053d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5053d-102">SYNOPSIS</span></span>
<span data-ttu-id="5053d-103">Ottiene le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5053d-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="5053d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5053d-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5053d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5053d-105">DESCRIPTION</span></span>
<span data-ttu-id="5053d-106">Il cmdlet **Get-AzDeletedWebApp** restituisce tutte le app Web eliminate nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5053d-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="5053d-107">Le app eliminate possono essere filtrate facoltativamente dal gruppo di risorse, dal nome e dallo slot.</span><span class="sxs-lookup"><span data-stu-id="5053d-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="5053d-108">Può essere presente più di un'app eliminata con lo stesso nome e il relativo gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5053d-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="5053d-109">Selezionare la DeletionTime per distinguere le app eliminate che condividono lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="5053d-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="5053d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5053d-110">EXAMPLES</span></span>

### <span data-ttu-id="5053d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5053d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="5053d-112">Questo comando consente di ottenere le app eliminate denominate ContosoSite appartenenti al gruppo di risorse default-Web-Westus.</span><span class="sxs-lookup"><span data-stu-id="5053d-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5053d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5053d-113">PARAMETERS</span></span>

### <span data-ttu-id="5053d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5053d-114">-DefaultProfile</span></span>
<span data-ttu-id="5053d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5053d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5053d-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5053d-116">-Location</span></span>
<span data-ttu-id="5053d-117">Posizione dell'app eliminata.</span><span class="sxs-lookup"><span data-stu-id="5053d-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="5053d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5053d-118">-Name</span></span>
<span data-ttu-id="5053d-119">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="5053d-119">The name of the web app.</span></span>

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

### <span data-ttu-id="5053d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5053d-120">-ResourceGroupName</span></span>
<span data-ttu-id="5053d-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5053d-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="5053d-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="5053d-122">-Slot</span></span>
<span data-ttu-id="5053d-123">Il nome dello slot Web App.</span><span class="sxs-lookup"><span data-stu-id="5053d-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="5053d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5053d-124">CommonParameters</span></span>
<span data-ttu-id="5053d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5053d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5053d-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5053d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5053d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5053d-127">INPUTS</span></span>

### <span data-ttu-id="5053d-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5053d-128">None</span></span>

## <span data-ttu-id="5053d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5053d-129">OUTPUTS</span></span>

### <span data-ttu-id="5053d-130">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5053d-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="5053d-131">Note</span><span class="sxs-lookup"><span data-stu-id="5053d-131">NOTES</span></span>

## <span data-ttu-id="5053d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5053d-132">RELATED LINKS</span></span>

[<span data-ttu-id="5053d-133">Ripristinare-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="5053d-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)