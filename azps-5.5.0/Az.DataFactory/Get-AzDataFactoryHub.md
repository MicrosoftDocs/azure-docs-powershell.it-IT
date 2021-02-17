---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198887"
---
# <span data-ttu-id="6d059-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="6d059-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="6d059-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d059-102">SYNOPSIS</span></span>
<span data-ttu-id="6d059-103">Ottiene informazioni sugli hub in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d059-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="6d059-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d059-104">SYNTAX</span></span>

### <span data-ttu-id="6d059-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="6d059-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d059-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6d059-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d059-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d059-107">DESCRIPTION</span></span>
<span data-ttu-id="6d059-108">Il **cmdlet Get-AzDataFactoryHub** ottiene informazioni sugli hub in Data factory di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d059-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="6d059-109">Se si specifica il nome di un hub, questo cmdlet ottiene informazioni sull'hub.</span><span class="sxs-lookup"><span data-stu-id="6d059-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="6d059-110">Se non si specifica un nome, questo cmdlet ottiene informazioni su tutti gli hub in un data factory.</span><span class="sxs-lookup"><span data-stu-id="6d059-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="6d059-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d059-111">EXAMPLES</span></span>

### <span data-ttu-id="6d059-112">Esempio 1: Ottenere tutti gli hub dati</span><span class="sxs-lookup"><span data-stu-id="6d059-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="6d059-113">Questo comando recupera tutti gli hub dati nel gruppo di risorse azure denominato ADFResourceGroup e il data factory denominato ADFDataWith.</span><span class="sxs-lookup"><span data-stu-id="6d059-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="6d059-114">Esempio 2: Ottenere un hub dati specifico</span><span class="sxs-lookup"><span data-stu-id="6d059-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="6d059-115">Questo comando recupera informazioni sull'hub denominato MyDataHub nel gruppo di risorse azure denominato ADFResourceGroup e sul data factory denominato ADFDataWith.</span><span class="sxs-lookup"><span data-stu-id="6d059-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="6d059-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d059-116">PARAMETERS</span></span>

### <span data-ttu-id="6d059-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d059-117">-DataFactory</span></span>
<span data-ttu-id="6d059-118">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="6d059-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6d059-119">Questo cmdlet ottiene informazioni sugli hub nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6d059-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d059-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6d059-120">-DataFactoryName</span></span>
<span data-ttu-id="6d059-121">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="6d059-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6d059-122">Questo cmdlet ottiene informazioni sugli hub nel data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6d059-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d059-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d059-123">-DefaultProfile</span></span>
<span data-ttu-id="6d059-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6d059-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d059-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6d059-125">-Name</span></span>
<span data-ttu-id="6d059-126">Specifica il nome dell'hub su cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="6d059-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d059-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d059-127">-ResourceGroupName</span></span>
<span data-ttu-id="6d059-128">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d059-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6d059-129">Questo cmdlet ottiene informazioni sugli hub appartenenti al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="6d059-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d059-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d059-130">CommonParameters</span></span>
<span data-ttu-id="6d059-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d059-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d059-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d059-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d059-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d059-133">INPUTS</span></span>

### <span data-ttu-id="6d059-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6d059-134">System.String</span></span>

### <span data-ttu-id="6d059-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6d059-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="6d059-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d059-136">OUTPUTS</span></span>

### <span data-ttu-id="6d059-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span><span class="sxs-lookup"><span data-stu-id="6d059-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="6d059-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d059-138">NOTES</span></span>
* <span data-ttu-id="6d059-139">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="6d059-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6d059-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d059-140">RELATED LINKS</span></span>

[<span data-ttu-id="6d059-141">New-AzDataHub</span><span class="sxs-lookup"><span data-stu-id="6d059-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="6d059-142">Remove-AzDataHub</span><span class="sxs-lookup"><span data-stu-id="6d059-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


