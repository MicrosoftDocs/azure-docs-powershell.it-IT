---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppCertificate.md
ms.openlocfilehash: e348d29a805de900aa3144832084e657cf85077c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364265"
---
# <span data-ttu-id="16ca9-101">Get-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="16ca9-101">Get-AzWebAppCertificate</span></span>

## <span data-ttu-id="16ca9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="16ca9-103">Ottiene un certificato di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="16ca9-103">Gets an Azure Web App certificate.</span></span>

## <span data-ttu-id="16ca9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16ca9-104">SYNTAX</span></span>

```
Get-AzWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ca9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="16ca9-106">Il cmdlet **Get-AzWebAppCertificate** ottiene le informazioni sui certificati di Azure Web App associati a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="16ca9-106">The **Get-AzWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="16ca9-107">Se si conosce l'identificazione personale del certificato, è possibile usare questo cmdlet anche per ottenere informazioni su un certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="16ca9-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="16ca9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16ca9-108">EXAMPLES</span></span>

### <span data-ttu-id="16ca9-109">Esempio 1: ottenere i certificati delle app Web in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="16ca9-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="16ca9-110">Questo comando restituisce informazioni sui certificati delle app Web caricati associati al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="16ca9-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="16ca9-111">Esempio 2: ottenere un certificato dell'app Web specificato</span><span class="sxs-lookup"><span data-stu-id="16ca9-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="16ca9-112">Questo comando ottiene il certificato dell'app Web ContosoResourceGroup con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="16ca9-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="16ca9-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16ca9-113">PARAMETERS</span></span>

### <span data-ttu-id="16ca9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ca9-114">-DefaultProfile</span></span>
<span data-ttu-id="16ca9-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16ca9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ca9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ca9-116">-ResourceGroupName</span></span>
<span data-ttu-id="16ca9-117">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="16ca9-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="16ca9-118">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="16ca9-118">-Thumbprint</span></span>
<span data-ttu-id="16ca9-119">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="16ca9-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="16ca9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ca9-120">CommonParameters</span></span>
<span data-ttu-id="16ca9-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16ca9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ca9-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16ca9-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ca9-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16ca9-123">INPUTS</span></span>

### <span data-ttu-id="16ca9-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16ca9-124">None</span></span>

## <span data-ttu-id="16ca9-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16ca9-125">OUTPUTS</span></span>

### <span data-ttu-id="16ca9-126">Microsoft. Azure. Commands. webapps. Models. Web App. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="16ca9-126">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="16ca9-127">Note</span><span class="sxs-lookup"><span data-stu-id="16ca9-127">NOTES</span></span>

## <span data-ttu-id="16ca9-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16ca9-128">RELATED LINKS</span></span>

[<span data-ttu-id="16ca9-129">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="16ca9-129">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)


