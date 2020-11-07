---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865797"
---
# <span data-ttu-id="746e7-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="746e7-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="746e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="746e7-102">SYNOPSIS</span></span>
<span data-ttu-id="746e7-103">Elimina l'emittente di un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="746e7-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="746e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="746e7-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="746e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="746e7-105">DESCRIPTION</span></span>
<span data-ttu-id="746e7-106">Il cmdlet **Remove-AzureKeyVaultCertificateIssuer** Elimina un emittente di certificati da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="746e7-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="746e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="746e7-107">EXAMPLES</span></span>

### <span data-ttu-id="746e7-108">Esempio 1: rimuovere un emittente di certificati</span><span class="sxs-lookup"><span data-stu-id="746e7-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="746e7-109">Questo comando rimuove l'autorità di certificazione denominata TestIssuer01 dal Vault della chiave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="746e7-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="746e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="746e7-110">PARAMETERS</span></span>

### <span data-ttu-id="746e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746e7-111">-DefaultProfile</span></span>
<span data-ttu-id="746e7-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="746e7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="746e7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="746e7-113">-Force</span></span>
<span data-ttu-id="746e7-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="746e7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="746e7-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="746e7-115">-Name</span></span>
<span data-ttu-id="746e7-116">Specifica il nome dell'emittente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="746e7-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="746e7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="746e7-117">-PassThru</span></span>
<span data-ttu-id="746e7-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="746e7-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="746e7-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="746e7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="746e7-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="746e7-120">-VaultName</span></span>
<span data-ttu-id="746e7-121">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="746e7-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="746e7-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="746e7-122">-Confirm</span></span>
<span data-ttu-id="746e7-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="746e7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="746e7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="746e7-124">-WhatIf</span></span>
<span data-ttu-id="746e7-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="746e7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746e7-126">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="746e7-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="746e7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="746e7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="746e7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746e7-128">CommonParameters</span></span>
<span data-ttu-id="746e7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746e7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746e7-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="746e7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746e7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="746e7-131">INPUTS</span></span>

## <span data-ttu-id="746e7-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="746e7-132">OUTPUTS</span></span>

### <span data-ttu-id="746e7-133">Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="746e7-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="746e7-134">Note</span><span class="sxs-lookup"><span data-stu-id="746e7-134">NOTES</span></span>

## <span data-ttu-id="746e7-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="746e7-135">RELATED LINKS</span></span>

[<span data-ttu-id="746e7-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="746e7-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="746e7-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="746e7-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


