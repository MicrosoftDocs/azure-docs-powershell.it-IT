---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: af7184b3e43d2016ff4acc9e7634f831945a8fdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519967"
---
# <span data-ttu-id="c35ee-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="c35ee-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="c35ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c35ee-102">SYNOPSIS</span></span>
<span data-ttu-id="c35ee-103">Scarica il profilo per un gateway di gestione server e lo salva in un file locale.</span><span class="sxs-lookup"><span data-stu-id="c35ee-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c35ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c35ee-104">SYNTAX</span></span>

### <span data-ttu-id="c35ee-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c35ee-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c35ee-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c35ee-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c35ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c35ee-107">DESCRIPTION</span></span>
<span data-ttu-id="c35ee-108">Il cmdlet **Save-AzureRmServerManagementGatewayProfile** Scarica il profilo per un gateway di gestione di Azure server e lo archivia in un file locale.</span><span class="sxs-lookup"><span data-stu-id="c35ee-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="c35ee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c35ee-109">EXAMPLES</span></span>

## <span data-ttu-id="c35ee-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c35ee-110">PARAMETERS</span></span>

### <span data-ttu-id="c35ee-111">-Gateway</span><span class="sxs-lookup"><span data-stu-id="c35ee-111">-Gateway</span></span>
<span data-ttu-id="c35ee-112">Specifica il gateway per cui questo cmdlet ottiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="c35ee-112">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="c35ee-113">Può essere usato invece di specificare ResourceGroupName e GatewayName</span><span class="sxs-lookup"><span data-stu-id="c35ee-113">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c35ee-114">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="c35ee-114">-GatewayName</span></span>
<span data-ttu-id="c35ee-115">Specifica il nome del gateway per cui questo cmdlet ottiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="c35ee-115">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c35ee-116">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="c35ee-116">-OutputFile</span></span>
<span data-ttu-id="c35ee-117">Specifica il file locale in cui salvare i dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="c35ee-117">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c35ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="c35ee-119">Specifica il nome del gruppo di risorse a cui appartiene il gateway.</span><span class="sxs-lookup"><span data-stu-id="c35ee-119">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c35ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c35ee-120">-DefaultProfile</span></span>
<span data-ttu-id="c35ee-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c35ee-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c35ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c35ee-122">CommonParameters</span></span>
<span data-ttu-id="c35ee-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c35ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c35ee-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c35ee-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c35ee-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c35ee-125">INPUTS</span></span>

### <span data-ttu-id="c35ee-126">Gateway</span><span class="sxs-lookup"><span data-stu-id="c35ee-126">Gateway</span></span>
<span data-ttu-id="c35ee-127">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c35ee-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="c35ee-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c35ee-128">OUTPUTS</span></span>

### <span data-ttu-id="c35ee-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="c35ee-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="c35ee-130">Note</span><span class="sxs-lookup"><span data-stu-id="c35ee-130">NOTES</span></span>

## <span data-ttu-id="c35ee-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c35ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="c35ee-132">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="c35ee-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="c35ee-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="c35ee-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


