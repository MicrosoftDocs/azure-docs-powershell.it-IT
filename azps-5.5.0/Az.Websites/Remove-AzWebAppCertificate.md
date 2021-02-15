---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppCertificate.md
ms.openlocfilehash: 7988975daa512b44c71b17929f47d3318bfe192c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182431"
---
# <span data-ttu-id="a51e1-101">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a51e1-101">Remove-AzWebAppCertificate</span></span>

## <span data-ttu-id="a51e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a51e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a51e1-103">Crea un certificato gestito del servizio app per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="a51e1-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="a51e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a51e1-104">SYNTAX</span></span>

```
Remove-AzWebAppCertificate [-ResourceGroupName] <String> [-ThumbPrint] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a51e1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a51e1-105">DESCRIPTION</span></span>
<span data-ttu-id="a51e1-106">Il cmdlet **Remove-AzWebAppCertificate** crea un certificato gestito del servizio app di Azure</span><span class="sxs-lookup"><span data-stu-id="a51e1-106">The **Remove-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>

## <span data-ttu-id="a51e1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a51e1-107">EXAMPLES</span></span>

### <span data-ttu-id="a51e1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a51e1-108">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 
```

<span data-ttu-id="a51e1-109">Questo comando rimuove il certificato gestito dal servizio app per l'app Web specificata.</span><span class="sxs-lookup"><span data-stu-id="a51e1-109">This command removes App Service Managed certificate for the given web app.</span></span>

## <span data-ttu-id="a51e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a51e1-110">PARAMETERS</span></span>

### <span data-ttu-id="a51e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51e1-111">-DefaultProfile</span></span>
<span data-ttu-id="a51e1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a51e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51e1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a51e1-113">-ResourceGroupName</span></span>
<span data-ttu-id="a51e1-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a51e1-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51e1-115">-ThumbPrint</span><span class="sxs-lookup"><span data-stu-id="a51e1-115">-ThumbPrint</span></span>
<span data-ttu-id="a51e1-116">Thumbprint del certificato già esistente nello spazio Web.</span><span class="sxs-lookup"><span data-stu-id="a51e1-116">Thumbprint of the certificate that already exists in web space.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51e1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51e1-117">CommonParameters</span></span>
<span data-ttu-id="a51e1-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a51e1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51e1-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a51e1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51e1-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="a51e1-120">INPUTS</span></span>

### <span data-ttu-id="a51e1-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a51e1-121">None</span></span>

## <span data-ttu-id="a51e1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a51e1-122">OUTPUTS</span></span>

### <span data-ttu-id="a51e1-123">System.Void</span><span class="sxs-lookup"><span data-stu-id="a51e1-123">System.Void</span></span>

## <span data-ttu-id="a51e1-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="a51e1-124">NOTES</span></span>

## <span data-ttu-id="a51e1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a51e1-125">RELATED LINKS</span></span>
[<span data-ttu-id="a51e1-126">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="a51e1-126">New-AzWebAppCertificate</span></span>](./New-AzWebAppCertificate.md)
