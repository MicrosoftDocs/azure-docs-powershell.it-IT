---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 52d40ed69adda157a8fdacd9d6c961f88508fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673644"
---
# <span data-ttu-id="b353f-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b353f-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="b353f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b353f-102">SYNOPSIS</span></span>
<span data-ttu-id="b353f-103">Ottiene i certificati di gestione delle API configurati per l'autenticazione reciproca con backend nel servizio.</span><span class="sxs-lookup"><span data-stu-id="b353f-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="b353f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b353f-104">SYNTAX</span></span>

### <span data-ttu-id="b353f-105">GetAllCertificates (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b353f-105">GetAllCertificates (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b353f-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="b353f-106">GetByCertificateId</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b353f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b353f-107">DESCRIPTION</span></span>
<span data-ttu-id="b353f-108">Il cmdlet **Get-AzApiManagementCertificate** ottiene tutti i certificati o i certificati di gestione delle API di Azure specificati.</span><span class="sxs-lookup"><span data-stu-id="b353f-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="b353f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b353f-109">EXAMPLES</span></span>

### <span data-ttu-id="b353f-110">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="b353f-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="b353f-111">Questo comando ottiene tutti i certificati di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="b353f-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="b353f-112">Esempio 2: ottenere un certificato in base all'ID</span><span class="sxs-lookup"><span data-stu-id="b353f-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="b353f-113">Questo comando ottiene il certificato di gestione delle API con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="b353f-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="b353f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b353f-114">PARAMETERS</span></span>

### <span data-ttu-id="b353f-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b353f-115">-CertificateId</span></span>
<span data-ttu-id="b353f-116">Specifica l'ID del certificato da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b353f-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b353f-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b353f-117">-Context</span></span>
<span data-ttu-id="b353f-118">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b353f-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b353f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b353f-119">-DefaultProfile</span></span>
<span data-ttu-id="b353f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b353f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b353f-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b353f-121">-Confirm</span></span>
<span data-ttu-id="b353f-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b353f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b353f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b353f-123">-WhatIf</span></span>
<span data-ttu-id="b353f-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b353f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b353f-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b353f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b353f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b353f-126">CommonParameters</span></span>
<span data-ttu-id="b353f-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b353f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b353f-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b353f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b353f-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b353f-129">INPUTS</span></span>

### <span data-ttu-id="b353f-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b353f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b353f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b353f-131">System.String</span></span>

## <span data-ttu-id="b353f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b353f-132">OUTPUTS</span></span>

### <span data-ttu-id="b353f-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b353f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="b353f-134">Note</span><span class="sxs-lookup"><span data-stu-id="b353f-134">NOTES</span></span>

## <span data-ttu-id="b353f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b353f-135">RELATED LINKS</span></span>

[<span data-ttu-id="b353f-136">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b353f-136">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="b353f-137">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b353f-137">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="b353f-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b353f-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


