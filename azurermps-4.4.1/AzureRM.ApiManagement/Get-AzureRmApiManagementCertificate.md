---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517271"
---
# <span data-ttu-id="8bbc4-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8bbc4-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="8bbc4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8bbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="8bbc4-103">Ottiene i certificati di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bbc4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bbc4-104">SYNTAX</span></span>

### <span data-ttu-id="8bbc4-105">Ottenere tutti i certificati (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8bbc4-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bbc4-106">Ottenere il certificato in base all'ID</span><span class="sxs-lookup"><span data-stu-id="8bbc4-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bbc4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bbc4-107">DESCRIPTION</span></span>
<span data-ttu-id="8bbc4-108">Il cmdlet **Get-AzureRmApiManagementCertificate** ottiene tutti i certificati o i certificati di gestione delle API di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="8bbc4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bbc4-109">EXAMPLES</span></span>

### <span data-ttu-id="8bbc4-110">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="8bbc4-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="8bbc4-111">Questo comando ottiene tutti i certificati di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="8bbc4-112">Esempio 2: ottenere un certificato in base all'ID</span><span class="sxs-lookup"><span data-stu-id="8bbc4-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="8bbc4-113">Questo comando ottiene il certificato di gestione delle API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="8bbc4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8bbc4-114">PARAMETERS</span></span>

### <span data-ttu-id="8bbc4-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="8bbc4-115">-CertificateId</span></span>
<span data-ttu-id="8bbc4-116">Specifica l'ID del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bbc4-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8bbc4-117">-Context</span></span>
<span data-ttu-id="8bbc4-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8bbc4-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bbc4-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8bbc4-119">-Confirm</span></span>
<span data-ttu-id="8bbc4-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbc4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bbc4-121">-WhatIf</span></span>
<span data-ttu-id="8bbc4-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bbc4-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbc4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bbc4-124">-DefaultProfile</span></span>
<span data-ttu-id="8bbc4-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bbc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bbc4-126">CommonParameters</span></span>
<span data-ttu-id="8bbc4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bbc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bbc4-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bbc4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bbc4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8bbc4-129">INPUTS</span></span>

## <span data-ttu-id="8bbc4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bbc4-130">OUTPUTS</span></span>

### <span data-ttu-id="8bbc4-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8bbc4-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="8bbc4-132">Note</span><span class="sxs-lookup"><span data-stu-id="8bbc4-132">NOTES</span></span>

## <span data-ttu-id="8bbc4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bbc4-133">RELATED LINKS</span></span>

[<span data-ttu-id="8bbc4-134">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8bbc4-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8bbc4-135">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8bbc4-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="8bbc4-136">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="8bbc4-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


