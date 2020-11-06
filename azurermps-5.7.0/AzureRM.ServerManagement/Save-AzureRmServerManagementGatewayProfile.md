---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512295"
---
# <span data-ttu-id="23ce5-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="23ce5-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="23ce5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="23ce5-103">Scarica il profilo per un gateway di gestione server e lo salva in un file locale.</span><span class="sxs-lookup"><span data-stu-id="23ce5-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23ce5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23ce5-104">SYNTAX</span></span>

### <span data-ttu-id="23ce5-105">ByName</span><span class="sxs-lookup"><span data-stu-id="23ce5-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ce5-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="23ce5-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ce5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23ce5-107">DESCRIPTION</span></span>
<span data-ttu-id="23ce5-108">Il cmdlet **Save-AzureRmServerManagementGatewayProfile** Scarica il profilo per un gateway di gestione di Azure server e lo archivia in un file locale.</span><span class="sxs-lookup"><span data-stu-id="23ce5-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="23ce5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23ce5-109">EXAMPLES</span></span>

## <span data-ttu-id="23ce5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23ce5-110">PARAMETERS</span></span>

### <span data-ttu-id="23ce5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ce5-111">-DefaultProfile</span></span>
<span data-ttu-id="23ce5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23ce5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23ce5-113">-Gateway</span><span class="sxs-lookup"><span data-stu-id="23ce5-113">-Gateway</span></span>
<span data-ttu-id="23ce5-114">Specifica il gateway per cui questo cmdlet ottiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="23ce5-114">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="23ce5-115">Può essere usato invece di specificare ResourceGroupName e GatewayName</span><span class="sxs-lookup"><span data-stu-id="23ce5-115">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ce5-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="23ce5-116">-GatewayName</span></span>
<span data-ttu-id="23ce5-117">Specifica il nome del gateway per cui questo cmdlet ottiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="23ce5-117">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ce5-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="23ce5-118">-OutputFile</span></span>
<span data-ttu-id="23ce5-119">Specifica il file locale in cui salvare i dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="23ce5-119">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ce5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ce5-120">-ResourceGroupName</span></span>
<span data-ttu-id="23ce5-121">Specifica il nome del gruppo di risorse a cui appartiene il gateway.</span><span class="sxs-lookup"><span data-stu-id="23ce5-121">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ce5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ce5-122">CommonParameters</span></span>
<span data-ttu-id="23ce5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ce5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ce5-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ce5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ce5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23ce5-125">INPUTS</span></span>

### <span data-ttu-id="23ce5-126">Gateway</span><span class="sxs-lookup"><span data-stu-id="23ce5-126">Gateway</span></span>
<span data-ttu-id="23ce5-127">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="23ce5-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="23ce5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23ce5-128">OUTPUTS</span></span>

### <span data-ttu-id="23ce5-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="23ce5-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="23ce5-130">Note</span><span class="sxs-lookup"><span data-stu-id="23ce5-130">NOTES</span></span>

## <span data-ttu-id="23ce5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23ce5-131">RELATED LINKS</span></span>

[<span data-ttu-id="23ce5-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="23ce5-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="23ce5-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="23ce5-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


