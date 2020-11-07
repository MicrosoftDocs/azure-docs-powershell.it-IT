---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861262"
---
# <span data-ttu-id="da738-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da738-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="da738-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da738-102">SYNOPSIS</span></span>
<span data-ttu-id="da738-103">Elimina un'operazione di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="da738-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="da738-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da738-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da738-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da738-105">DESCRIPTION</span></span>
<span data-ttu-id="da738-106">Il cmdlet **Remove-AzKeyVaultCertificateOperation** Elimina un'operazione di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="da738-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="da738-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da738-107">EXAMPLES</span></span>

### <span data-ttu-id="da738-108">Esempio 1: rimuovere un'operazione di certificato</span><span class="sxs-lookup"><span data-stu-id="da738-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="da738-109">Questo comando rimuove l'operazione di certificato denominata TestCert01 dall'archivio della chiave ContosoKV01 senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="da738-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="da738-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da738-110">PARAMETERS</span></span>

### <span data-ttu-id="da738-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da738-111">-DefaultProfile</span></span>
<span data-ttu-id="da738-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="da738-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da738-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da738-113">-Force</span></span>
<span data-ttu-id="da738-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="da738-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da738-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="da738-115">-Name</span></span>
<span data-ttu-id="da738-116">Specifica il nome di un certificato.</span><span class="sxs-lookup"><span data-stu-id="da738-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da738-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da738-117">-PassThru</span></span>
<span data-ttu-id="da738-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="da738-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da738-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="da738-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da738-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="da738-120">-VaultName</span></span>
<span data-ttu-id="da738-121">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="da738-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da738-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da738-122">-Confirm</span></span>
<span data-ttu-id="da738-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da738-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da738-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da738-124">-WhatIf</span></span>
<span data-ttu-id="da738-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da738-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da738-126">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da738-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da738-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da738-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da738-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da738-128">CommonParameters</span></span>
<span data-ttu-id="da738-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da738-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da738-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da738-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da738-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da738-131">INPUTS</span></span>

### <span data-ttu-id="da738-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da738-132">None</span></span>
<span data-ttu-id="da738-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="da738-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da738-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da738-134">OUTPUTS</span></span>

### <span data-ttu-id="da738-135">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da738-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="da738-136">Note</span><span class="sxs-lookup"><span data-stu-id="da738-136">NOTES</span></span>

## <span data-ttu-id="da738-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da738-137">RELATED LINKS</span></span>

[<span data-ttu-id="da738-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da738-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="da738-139">Stop-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="da738-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

