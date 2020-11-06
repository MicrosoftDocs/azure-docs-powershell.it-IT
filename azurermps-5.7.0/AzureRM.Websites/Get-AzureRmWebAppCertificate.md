---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: e2aaa6ed6e66e61f8d62f1235ff8e2a8ff9f65e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509535"
---
# <span data-ttu-id="f4da8-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="f4da8-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="f4da8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4da8-102">SYNOPSIS</span></span>
<span data-ttu-id="f4da8-103">Ottiene un certificato di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f4da8-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4da8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4da8-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4da8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4da8-105">DESCRIPTION</span></span>
<span data-ttu-id="f4da8-106">Il cmdlet **Get-AzureRmWebAppCertificate** ottiene le informazioni sui certificati di Azure Web App associati a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="f4da8-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="f4da8-107">Se si conosce l'identificazione personale del certificato, è possibile usare questo cmdlet anche per ottenere informazioni su un certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="f4da8-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="f4da8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4da8-108">EXAMPLES</span></span>

### <span data-ttu-id="f4da8-109">Esempio 1: ottenere i certificati delle app Web in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f4da8-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f4da8-110">Questo comando restituisce informazioni sui certificati delle app Web caricati associati al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f4da8-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="f4da8-111">Esempio 2: ottenere un certificato dell'app Web specificato</span><span class="sxs-lookup"><span data-stu-id="f4da8-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="f4da8-112">Questo comando ottiene il certificato dell'app Web ContosoResourceGroup con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="f4da8-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="f4da8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4da8-113">PARAMETERS</span></span>

### <span data-ttu-id="f4da8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4da8-114">-DefaultProfile</span></span>
<span data-ttu-id="f4da8-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4da8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4da8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4da8-116">-ResourceGroupName</span></span>
<span data-ttu-id="f4da8-117">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="f4da8-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4da8-118">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="f4da8-118">-Thumbprint</span></span>
<span data-ttu-id="f4da8-119">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="f4da8-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4da8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4da8-120">CommonParameters</span></span>
<span data-ttu-id="f4da8-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4da8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4da8-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4da8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4da8-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4da8-123">INPUTS</span></span>

### <span data-ttu-id="f4da8-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4da8-124">None</span></span>
<span data-ttu-id="f4da8-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f4da8-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4da8-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4da8-126">OUTPUTS</span></span>

## <span data-ttu-id="f4da8-127">Note</span><span class="sxs-lookup"><span data-stu-id="f4da8-127">NOTES</span></span>

## <span data-ttu-id="f4da8-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4da8-128">RELATED LINKS</span></span>

[<span data-ttu-id="f4da8-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f4da8-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


