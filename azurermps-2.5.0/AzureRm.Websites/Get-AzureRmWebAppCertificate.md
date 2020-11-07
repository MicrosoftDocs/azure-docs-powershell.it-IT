---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
ms.openlocfilehash: dcdba23de872ed0f1518188387c6f7e2d357c909
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865991"
---
# <span data-ttu-id="07cfe-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="07cfe-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="07cfe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07cfe-102">SYNOPSIS</span></span>
<span data-ttu-id="07cfe-103">Ottiene un certificato di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="07cfe-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07cfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07cfe-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07cfe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07cfe-105">DESCRIPTION</span></span>
<span data-ttu-id="07cfe-106">Il cmdlet **Get-AzureRmWebAppCertificate** ottiene le informazioni sui certificati di Azure Web App associati a un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="07cfe-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="07cfe-107">Se si conosce l'identificazione personale del certificato, è possibile usare questo cmdlet anche per ottenere informazioni su un certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="07cfe-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="07cfe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07cfe-108">EXAMPLES</span></span>

### <span data-ttu-id="07cfe-109">Esempio 1: ottenere i certificati delle app Web in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="07cfe-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="07cfe-110">Questo comando restituisce informazioni sui certificati delle app Web caricati associati al gruppo di risorse ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="07cfe-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="07cfe-111">Esempio 2: ottenere un certificato dell'app Web specificato</span><span class="sxs-lookup"><span data-stu-id="07cfe-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="07cfe-112">Questo comando ottiene il certificato dell'app Web ContosoResourceGroup con l'identificazione personale E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="07cfe-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="07cfe-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07cfe-113">PARAMETERS</span></span>

### <span data-ttu-id="07cfe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07cfe-114">-DefaultProfile</span></span>
<span data-ttu-id="07cfe-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07cfe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07cfe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07cfe-116">-ResourceGroupName</span></span>
<span data-ttu-id="07cfe-117">Specifica il nome del gruppo di risorse a cui è assegnato il certificato.</span><span class="sxs-lookup"><span data-stu-id="07cfe-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="07cfe-118">-Identificazione personale</span><span class="sxs-lookup"><span data-stu-id="07cfe-118">-Thumbprint</span></span>
<span data-ttu-id="07cfe-119">Specifica l'identificatore univoco per il certificato.</span><span class="sxs-lookup"><span data-stu-id="07cfe-119">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="07cfe-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07cfe-120">CommonParameters</span></span>
<span data-ttu-id="07cfe-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07cfe-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07cfe-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07cfe-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07cfe-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07cfe-123">INPUTS</span></span>

### <span data-ttu-id="07cfe-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="07cfe-124">None</span></span>
<span data-ttu-id="07cfe-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="07cfe-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07cfe-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07cfe-126">OUTPUTS</span></span>

## <span data-ttu-id="07cfe-127">Note</span><span class="sxs-lookup"><span data-stu-id="07cfe-127">NOTES</span></span>

## <span data-ttu-id="07cfe-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07cfe-128">RELATED LINKS</span></span>

[<span data-ttu-id="07cfe-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="07cfe-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


