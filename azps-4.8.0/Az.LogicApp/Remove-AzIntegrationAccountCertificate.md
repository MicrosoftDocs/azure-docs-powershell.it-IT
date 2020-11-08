---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 78bf9f5e61a66aee6c34dbeb7002d4b2e88e3b68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189774"
---
# <span data-ttu-id="b0300-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b0300-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="b0300-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0300-102">SYNOPSIS</span></span>
<span data-ttu-id="b0300-103">Rimuove un certificato dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0300-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="b0300-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0300-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0300-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0300-105">DESCRIPTION</span></span>
<span data-ttu-id="b0300-106">Il cmdlet **Remove-AzIntegrationAccountCertificate** rimuove un certificato dell'account di integrazione da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0300-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="b0300-107">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="b0300-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="b0300-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="b0300-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b0300-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="b0300-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b0300-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b0300-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b0300-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="b0300-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b0300-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0300-112">EXAMPLES</span></span>

### <span data-ttu-id="b0300-113">Esempio 1: rimuovere un certificato dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="b0300-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="b0300-114">Questo comando rimuove il certificato dell'account di integrazione denominato IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="b0300-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="b0300-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0300-115">PARAMETERS</span></span>

### <span data-ttu-id="b0300-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="b0300-116">-CertificateName</span></span>
<span data-ttu-id="b0300-117">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0300-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="b0300-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0300-118">-DefaultProfile</span></span>
<span data-ttu-id="b0300-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b0300-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0300-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b0300-120">-Force</span></span>
<span data-ttu-id="b0300-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b0300-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0300-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0300-122">-Name</span></span>
<span data-ttu-id="b0300-123">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="b0300-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b0300-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0300-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0300-125">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0300-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b0300-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0300-126">-Confirm</span></span>
<span data-ttu-id="b0300-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0300-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0300-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0300-128">-WhatIf</span></span>
<span data-ttu-id="b0300-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0300-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0300-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0300-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0300-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0300-131">CommonParameters</span></span>
<span data-ttu-id="b0300-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0300-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0300-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0300-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0300-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0300-134">INPUTS</span></span>

### <span data-ttu-id="b0300-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b0300-135">System.String</span></span>

## <span data-ttu-id="b0300-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0300-136">OUTPUTS</span></span>

### <span data-ttu-id="b0300-137">System. void</span><span class="sxs-lookup"><span data-stu-id="b0300-137">System.Void</span></span>

## <span data-ttu-id="b0300-138">Note</span><span class="sxs-lookup"><span data-stu-id="b0300-138">NOTES</span></span>

## <span data-ttu-id="b0300-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0300-139">RELATED LINKS</span></span>

[<span data-ttu-id="b0300-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b0300-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b0300-141">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b0300-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="b0300-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="b0300-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


