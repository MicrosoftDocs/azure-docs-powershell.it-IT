---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 71c910fafea0c555f5ba0d7a62573c2de2be3b41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520062"
---
# <span data-ttu-id="e812f-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e812f-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e812f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e812f-102">SYNOPSIS</span></span>
<span data-ttu-id="e812f-103">Rimuove un certificato dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e812f-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e812f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e812f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e812f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e812f-105">DESCRIPTION</span></span>
<span data-ttu-id="e812f-106">Il cmdlet **Remove-AzureRmIntegrationAccountCertificate** rimuove un certificato dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e812f-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="e812f-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="e812f-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="e812f-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="e812f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e812f-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="e812f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e812f-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="e812f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e812f-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="e812f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e812f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e812f-112">EXAMPLES</span></span>

### <span data-ttu-id="e812f-113">Esempio 1: rimuovere un certificato dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="e812f-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="e812f-114">Questo comando rimuove il certificato dell'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="e812f-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="e812f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e812f-115">PARAMETERS</span></span>

### <span data-ttu-id="e812f-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="e812f-116">-CertificateName</span></span>
<span data-ttu-id="e812f-117">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e812f-117">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e812f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e812f-118">-Force</span></span>
<span data-ttu-id="e812f-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e812f-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e812f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e812f-120">-Name</span></span>
<span data-ttu-id="e812f-121">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="e812f-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e812f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e812f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e812f-123">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e812f-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e812f-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e812f-124">-Confirm</span></span>
<span data-ttu-id="e812f-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e812f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e812f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e812f-126">-WhatIf</span></span>
<span data-ttu-id="e812f-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e812f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e812f-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e812f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e812f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e812f-129">-DefaultProfile</span></span>
<span data-ttu-id="e812f-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e812f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e812f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e812f-131">CommonParameters</span></span>
<span data-ttu-id="e812f-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e812f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e812f-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e812f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e812f-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e812f-134">INPUTS</span></span>

## <span data-ttu-id="e812f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e812f-135">OUTPUTS</span></span>

## <span data-ttu-id="e812f-136">Note</span><span class="sxs-lookup"><span data-stu-id="e812f-136">NOTES</span></span>

## <span data-ttu-id="e812f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e812f-137">RELATED LINKS</span></span>

[<span data-ttu-id="e812f-138">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e812f-138">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="e812f-139">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e812f-139">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="e812f-140">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e812f-140">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


